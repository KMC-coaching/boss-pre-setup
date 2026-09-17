---
name: set-up-my-computer
description: Prepares a brand-new student's computer to receive their Authority Operating System, before they have GitHub connected, before any files are on the machine, and without ever asking them to open a terminal or type a command. Settles what Claude is allowed to do, puts Git and the GitHub tool in place without admin rights, signs them in through their browser, confirms their access, brings their system down onto the machine, then hands off to the system's own setup. Use when the student says "set up my computer", "set me up", "get me started", "install my operating system", "set up my OS", "onboard me", "I just joined", or runs this plugin for the first time.
version: 1.0.0
---

# Set Up My Computer (step one of two)

## What this is, and where it stops

This runs on a computer that has nothing on it yet. No system folder, no GitHub
connection, no tools. It gets the machine ready and brings the system down, and then it
**stops and hands off**.

Everything after the system lands - personalizing it, building their Business Brain, the
smoke test, schedules, the diagnostic - belongs to `setup-my-os`, which arrives inside
the system itself. Do not do any of that here. Do not ask the questions it asks. The
handoff in Step 7 is the end of your job.

**If a system folder already exists on this machine, you are the wrong skill.** Say so in
one line and run `setup-my-os` instead.

## The two rules that matter more than the steps

### 1. They never type a command. Not once.

If you are about to say "open your terminal", "paste this", "run this command", or
"create this folder", stop. That sentence is the failure this skill exists to remove. You
have their computer; use it. The only things they do by hand are the three in Step 4,
because no software on earth can do those for them.

### 2. Their words, not yours

Never say: repository, repo, clone, fork, remote, commit, branch, terminal, shell, CLI,
command line, PATH, package manager, Homebrew, sudo, admin rights, token, scope, API,
binary, environment variable.

Their words are: **your system**, **your folder**, **your backup**, **the sign-in**,
**the tool that brings your system down**.

"Command" is allowed, because they will see that word in the approval box and pretending
it isn't there helps nobody.

---

## Step 0 - Say what is about to happen

> "Hi. I'm getting your computer ready for your operating system. Fifteen to twenty
> minutes, and I do nearly all of it.
>
> Two things so nothing surprises you. You'll see a lot scroll past, and sometimes the
> word **error**. That's normal, that's me finding something and fixing it. And a box
> will pop up asking whether to allow something - that's the Claude app asking, it's
> expected, and it is not a warning.
>
> When that box appears, pick the option that allows it **and says something like don't
> ask again**. The wording is slightly different depending on how you're running this, so
> go by what it means. Picking that once is the difference between a couple of taps and
> a few dozen.
>
> I'll only stop you for the one part I can't do myself: signing in to your own account.
>
> Ready?"

Wait for a yes.

**Never name an exact button.** What that box says depends on their version and how they
are running Claude. Describe what the option means and let them find it. A script that
names a button is wrong on half the machines it runs on, and it teaches them to distrust
everything else you say.

## Step 1 - Cut the number of boxes down to one

Before anything else, try to write the allow list. This is the single highest-value action
in this skill: it converts the next twenty approval boxes into zero.

Write to the **user-level** settings file, which applies in every folder they will ever
open, including this one and the system folder that does not exist yet:

- Mac and Linux: `~/.claude/settings.json`
- Windows: `%USERPROFILE%\.claude\settings.json`

**Merge, never overwrite.** If the file exists, read it, add only the entries below that
are missing, and write it back with everything else untouched. If it does not exist,
create it with just a `permissions.allow` block. Clobbering a file they already have is
how you break a setup that was working.

The entries to ensure are present:

```
"Read", "Write", "Edit", "Glob", "Grep",
"Bash(uname:*)", "Bash(sw_vers:*)", "Bash(command -v:*)", "Bash(which:*)",
"Bash(mkdir:*)", "Bash(ls:*)", "Bash(cat:*)", "Bash(cp:*)", "Bash(mv:*)",
"Bash(chmod:*)", "Bash(find:*)", "Bash(curl:*)", "Bash(unzip:*)", "Bash(tar:*)",
"Bash(git:*)", "Bash(gh:*)", "Bash(python3:*)", "Bash(xcode-select:*)",
"Bash(winget:*)"
```

That list is deliberately not `Bash(*)`. These are the least technical people who will
ever run this, and blanket-allowing everything removes the last thing standing between
them and a bad instruction later. Everything the install needs is above; nothing else is.

**If the write is refused,** do not argue with it and do not send them into a settings
screen. Say one line - *"I couldn't set that automatically, so you'll see a few more of
those allow boxes than I'd like. Same answer each time."* - and carry on. The install
still works, it is just tappier.

**Your own side of this.** Every separate command is another box. From here to the end,
group work into as few commands as you can. Run each step's check as one script, not as
a string of lookups. Never re-run something to confirm what the first command already
printed. Four approvals and twenty approvals do identical work; the difference is
entirely how you grouped them.

## Step 2 - Read the machine, once

One script. Not a series of questions to the computer.

Find out: the operating system, the processor family, whether Git is present, whether the
GitHub tool is present, whether a usable Python is present, and where their home folder
is. Print it as a short block and move on. Do not show them the raw output.

Everything downstream branches off this. Nothing downstream may assume Mac.

## Step 3 - Put the missing tools in place, without admin rights

Only install what Step 2 said was missing. Say one plain line before each
(*"Putting the tool in place that brings your system down - about a minute."*).

**Nothing here may need their computer password.** If a path you are considering needs
one, it is the wrong path. There is always another way, and the one below is it.

### Git

- **Mac:** `xcode-select --install`. This opens Apple's own installer window. It is the
  one place a dialog appears that is not Claude's, so tell them first: *"A window from
  Apple is about to open asking to install some tools. Click Install and let it finish -
  five to ten minutes, and it's the longest wait in this whole setup."* Poll until
  `git --version` answers, then continue.
- **Windows:** `winget install --id Git.Git --silent --accept-package-agreements
  --accept-source-agreements`.
- **Linux:** whichever of `apt-get`, `dnf` is present, user-scope where possible.

### The GitHub tool

Never install this through a package manager that wants a password.

- **Mac and Linux:** download the release archive for their processor family with `curl`,
  unpack it, and place the single program file in `~/.local/bin/`, creating that folder
  if needed. Make it runnable. Nothing leaves their home folder.
- **Windows:** `winget install --id GitHub.cli --silent --accept-package-agreements
  --accept-source-agreements`.

### After installing, the tool is there and the machine still cannot find it

This happens on every platform and it is the single most common reason a setup stalls
with "it says it can't find it." Verified on a bare Mac on 2026-09-17: the download
lands, the file is executable, and the shell still answers `command not found`.

- **Mac and Linux:** `~/.local/bin` is **not** on the default PATH. Installing there and
  then calling `gh` by name fails every time. For the rest of this install, call it by
  its full path (`$HOME/.local/bin/gh`), and never assume a bare `gh` will resolve. Also
  append that folder to their shell profile so it keeps working after today, but do not
  depend on that having taken effect in the session you are already inside.
- **Windows:** the environment is not re-read until a new session starts. Re-read it
  yourself in the session you are in, rather than telling them to close and reopen
  anything.

Whatever you do, verify by running the tool and seeing a version number come back before
you move on. A file existing on disk is not the same as the machine being able to run it,
and that gap is precisely what this step exists to close.

## Step 4 - The three things only they can do

These are the only human steps in the entire install. Do not attempt them yourself, and
do not apologise for them - they exist because they are theirs.

1. **Sign in to GitHub.** Do not improvise this command; it is the one step that is
   awkward to retry, and a wrong scope here fails later at the clone with an error that
   looks like a permissions problem instead of a sign-in problem.

   **First check whether they are already signed in.** `gh auth status`. Many students
   are, from something else. If they are signed in but missing scopes, top them up with
   `gh auth refresh` rather than making them sign in again.

   If they are not signed in, run the browser flow:

   ```
   gh auth login --hostname github.com --git-protocol https --web --scopes "repo,read:org,gist,workflow"
   ```

   `repo` is the one that matters - their system is private, and without it the clone in
   Step 6 fails. `read:org` and `gist` are the documented minimum alongside it; `workflow`
   saves a second sign-in later. Remember: after a home-folder install, `gh` is not on
   PATH, so call it by its full path.

   Tell them what is about to happen before it happens: *"A browser tab is opening. Sign
   in to your GitHub account, and approve it on your phone if it asks. Come back here
   when it says you're done."* Then wait. Do not run anything else while that tab is open.

   **Then run `gh auth setup-git`.** This lets the clone in Step 6 authenticate as them.
   Skipping it is a common cause of the clone failing right after a sign-in that plainly
   worked.

   **Confirm it landed** with `gh auth status` and check the account name that comes back
   is the one they expect, before moving on. If they have more than one GitHub account,
   this is where the wrong one gets caught - and Step 5 is where it otherwise shows up as
   a confusing "you don't have access" ten minutes later.
2. **Accept the invitation to their system.** They were sent one by email. If the access
   check in Step 5 fails, this is almost always why. Tell them to look for it, including
   in spam.
3. **Two-factor codes**, whenever their phone asks.

If they do not have a GitHub account at all, walk them through creating one in the
browser, then come back. Never create an account on their behalf and never handle their
password.

## Step 5 - Confirm they can actually reach their system

Check that their signed-in account can see the system they were given access to, before
trying to bring anything down. A failure here is one of exactly two things and you should
say both:

- The invitation has not been accepted yet - check email, including spam.
- They signed in as a different GitHub account than the one they were invited on.

Do not guess which. Tell them both and how to check each. Do not send them to anyone by
email. If it stays stuck, the routes are office hours, the group call, or the Facebook
group - screenshot first and hand the screenshot back here so this can be fixed in the
session.

## Step 6 - Bring their system down onto the machine

Make the folder that holds it, in their home folder, and bring the system down into it
under a name built from their business name. Ask for the business name in plain words if
it has not come up yet - *"What should I call your folder? Your business name is the
usual answer."*

Say one line when it lands. Do not show them the output.

## Step 7 - Hand off, and stop

The moment the system is on the machine, this skill is finished.

> "Your system is on your computer. Everything from here - making it yours, building your
> Business Brain, and putting it to work - is the system's own setup, and it's better at
> that than I am. Starting it now."

Then point Claude at the new folder and run `setup-my-os` from inside it. If the student
must re-open Claude on that folder first, tell them the one thing they will see:
*"It'll ask whether you trust this folder. Click Trust - that's expected, and it only
asks once."*

Do not re-ask anything `setup-my-os` asks. Do not personalize anything. Stop here.

---

## When something unexpected happens

Pick the safest option and keep going. Say one line about what you did. Do not stop to
hand them a technical decision they have no way to settle.

Safest means, in order: destroy nothing, touch none of their own files, prefer what can
be undone, prefer what needs no password, and prefer doing nothing over guessing at
something permanent.

The exception is anything irreversible or outside this machine - deleting something of
theirs, sending anything to another person, or spending money. Those stop and ask, every
time, in plain words.

## Never

- Never tell them to open a terminal, paste a command, or create a folder by hand.
- Never ask for their computer password, and never take a path that needs one.
- Never name an exact button in the approval box.
- Never write `Bash(*)` into their settings.
- Never overwrite an existing settings file instead of merging into it.
- Never give out an email address for support, and never suggest emailing anyone.
- Never continue past Step 7 into work that belongs to `setup-my-os`.
