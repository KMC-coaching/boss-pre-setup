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

### 3. She is nervous, alone, and nobody is sitting next to her

Assume a 60-year-old agent who has never installed anything, is already a little
overwhelmed, and has no one in the room to ask. She will not tell you she is lost. She
will go quiet, or say "ok", or guess. Everything below exists because of that.

**Say what is about to happen before it happens. Every time.** Never run something that
takes more than a few seconds without first saying, in one or two lines: what you are
about to do, what she will see on her screen, roughly how long, and what "normal" looks
like while it happens. A wait she was warned about is a wait. A wait she was not warned
about is a crash.

The shape, every time:

> "Next I'm going to [plain-English thing]. You'll see [what appears]. It takes about
> [time]. You don't need to do anything while it runs."

**Silence is the enemy.** If something takes longer than about thirty seconds, say
something while it runs. "Still going, this is the slow one" is worth more to her than a
correct but silent install.

**Tell her she can stop you, twice: once at the start, and again the moment she sounds
unsure.** These two sentences are not optional, and they are not decoration:

> "If anything I say doesn't make sense, tell me to explain it a different way. I won't
> think less of you for asking and there's no limit on how many times you can.
>
> And if you're ever unsure which option to pick, just ask me. I'll tell you which one
> and why."

**Never make her feel behind.** No "as you probably know", no "simply", no "just". If she
asks something basic, answer it like it is a good question, because for her it is. If she
apologises for asking, tell her plainly that she has nothing to apologise for.

### 4. Decide for her. Only ask when it is genuinely hers to answer.

Most of what comes up in this install is not a real choice. It is a technical fork with
one right answer, and handing it to her is how a person who was doing fine starts to feel
stupid.

- **If you know the right answer, do it.** Do not narrate the fork, do not ask
  permission, do not explain what you considered. Say what you did in one line afterwards
  if it matters at all.
- **If you must ask, never present a menu.** One recommended answer, stated plainly, with
  the reason in a half-sentence: *"I'd use your Gmail for this, because a brokerage
  address stops working the day you change brokerages. Sound alright?"* A yes is the
  expected answer.
- **Always give her a way out of deciding.** "Just do whatever you think is best" must
  always be an available answer, and when she says it, that is full permission. Take it
  and move on.

The only things that are genuinely hers: her business name, her own account and password,
which email her invitation went to, and anything irreversible. Everything else is yours.

### 5. The things that confuse people here, and what to say

These come up. Say the explanation **before** the moment, not after she has been staring
at it.

**A password box is not part of this, and here is the one place it could appear.**
Nothing in this install needs her computer password. Everything goes into her own home
folder and the browser sign-in is GitHub's, not her Mac's. If a box asking for her
computer password ever does appear, it is Apple's own installer on a locked-down or
work-managed machine, not something you did. Say so plainly, tell her it is safe to enter
it there because it is Apple's own window, and if she does not know it or does not want
to, say the install can continue without it and route around.

**She will never be typing a password into a black window where nothing appears.** That
happens in the terminal, this never uses the terminal, and you should not raise the fear
by explaining it. Only if she brings it up: tell her that is a different thing, it is not
part of this, and the reason nothing shows when you type there is deliberate, not broken.

**Apple's installer window looks frozen.** It shows almost no progress for five to ten
minutes. Warn her first, tell her it is the longest wait of the whole setup, and check in
while it runs so she knows you are still there.

**"error" on screen is you working, not her failing.** Say this at the start and again
the first time one appears.

**The one-time code is not a password.** She may hesitate to type a code into a web page.
Tell her what it is: a short code that proves this computer is hers, it is useless to
anyone else, and it stops working in a few minutes either way.

**A rejected code is not her fault.** Two ordinary causes, you cannot see which, a fresh
one costs nothing. Never let her sit with the idea that she typed it wrong and broke it.

**Nothing here costs money.** She may not ask, but she may be worrying. If money comes up
at all, answer it flatly: the tools are free, the account is free, you will not ask for a
card, and you will not sign her up for anything.

**A pause is not a failure.** If she has to stop and come back - a call, a showing, a
school run - tell her everything done so far stays done, and she can pick up by saying
the same words again.

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

**Copy it before you touch it, then merge, never overwrite.** If the file exists:

1. **Take a copy first** - `settings.json.bak` beside it. This is the one irreversible
   thing in the whole skill, and a copy costs nothing. Students who have used Claude
   before may have hooks, connectors and permissions in there that took them a long time
   to get right, and that no one can reconstruct for them.
2. Read it, add only the entries below that are missing, and write it back with
   everything else untouched.
3. Say plainly that their existing settings were kept and a copy was made.

If the file does not exist, create it with just a `permissions.allow` block, and say
there was nothing of theirs to merge into.

Clobbering a file they already have is how you break a setup that was working, and the
people most likely to have one are the least likely to forgive it.

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

**If they refuse a box, that is a correct answer and you say so.** Nothing was written,
nothing changed, and the system did what they wanted. Tell them what the command was for
in one plain sentence and let them decide again. Never re-run the same thing hoping for a
different answer, and never imply they have made the install harder - they have made it
slower, which is theirs to choose.

For a student who is plainly wary, it is worth offering to write the list of what you are
allowed to do somewhere they can read it, in their own words, before you do anything
else. If you do, be straight about what it is: it is your stated plan, not a lock. The
lock is them reading each box before they approve it. Overselling a reassurance to a
suspicious person is how you lose them for the rest of the install.

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

- **Mac and Linux:** **resolve the download address from the releases API - never
  construct it by hand.** There is no version-less "latest/download" file to guess at:
  the real filename carries the version number *and* the extension differs by platform
  (macOS ships `.zip`, Linux ships `.tar.gz`). A rehearsal on 2026-09-17 invented
  `latest/download/gh_macOS_arm64.tar.gz`, which does not exist and 404s.

  Ask the API which asset matches their platform and architecture, take the address it
  gives back, then download, unpack, and place the single program file in
  `~/.local/bin/`, creating that folder if needed. Make it runnable. Nothing leaves their
  home folder.

  If that lookup fails or is rate-limited, do not guess a URL. Say one line - *"The
  download list is busy, trying again"* - wait a few seconds and retry it. Only if it
  keeps failing, fall back to whichever package manager is already on the machine, and
  never install one.
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

   If they are not signed in, run the browser flow **in the background**, never in the
   foreground. Verified on 2026-09-17: inside a tool call there is no terminal attached,
   and this command prints the code and then blocks, polling, until the student finishes
   in their browser. Run in the foreground it looks frozen and eventually times out. Run
   in the background it works exactly as intended.

   ```
   gh auth login --hostname github.com --git-protocol https --web \
     --scopes "repo,read:org,gist,workflow" < /dev/null > /tmp/boss-signin.txt 2>&1 &
   ```

   Within a second or two that file contains, verbatim:

   ```
   ! First copy your one-time code: XXXX-XXXX
   Open this URL to continue in your web browser: https://github.com/login/device
   ```

   Read the code out of that file and **give it to them with the address, in one message**:

   > "Go to **github.com/login/device** and type in this code: **XXXX-XXXX**
   >
   > Sign in if it asks, approve on your phone if it asks, and come back here. I'll be
   > watching for it - you don't need to tell me when you're done."

   Say the address and the code and nothing else. Do not paste the raw output at them, do
   not explain what a one-time code is, and never ask them to run the command themselves.
   You generate the code; they type it in one box.

   Then **poll `gh auth status` until it comes back signed in.** Do not sit and wait on
   the background job.

   **If they report the code was rejected, do not assert why.** You cannot see what they
   typed, and there are two ordinary causes: a character mistyped, or the code went stale
   because a few minutes passed. Both are common and neither is their fault. Say both,
   and issue a fresh one immediately - a new code costs nothing and is faster than
   diagnosing the old one. A rehearsal on 2026-09-17 blamed expiry for what was actually
   a typo; the student is not harmed by that, but stating an unverified cause is how a
   confident wrong explanation gets believed later.

   Before issuing a fresh code, stop the previous attempt so two are not polling at once.
   **Stop it by name, not by job number.** Each command runs in its own shell, so `kill %1`
   refers to nothing and silently does nothing, leaving the old attempt alive to collide
   with the new one. Match the process instead:

   ```
   pkill -f "gh auth login" || true
   ```

   Then tell her the old code is dead and not to use it. A student holding two codes will
   try the wrong one, and it will look like the system is broken when it is only confused.

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

**Know which system you are looking for before you look.** There are two, and they are
not interchangeable:

| Who they are | Their system |
|---|---|
| Real estate agent, or lender (the default) | `Krista-Mashore-Coaching/Agent-Authority-Operating-System` |
| Any other professional or business owner | `Krista-Mashore-Coaching/Authority-Operating-System` |

If it is not obvious which they are, ask one plain question - *"Are you a real estate
agent, or something else?"* - and route on the answer. **Never invent a name and never
guess at one.** A rehearsal on 2026-09-17 made up a repository that does not exist and
would have failed at the last step, after the student had done all the work.

Confirm the account they just signed in as can actually see that system before trying to
bring anything down.

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

**The destination is not yours to choose.** `setup-my-os` takes over in Step 7 and it
expects the system in a specific place under a specific name. Put it anywhere else and
the handoff lands in a folder the next skill cannot find.

- Parent folder: `~/Sites/` on Mac and Linux, `Sites\` under their user folder on Windows
- Folder name: `BOSS-OS-<business-name>`, lowercased and hyphenated
- If that folder already exists, append `-2`, then `-3`. Do not ask which they prefer

Ask for the business name in plain words if it has not come up - *"What should I call
your folder? Your business name is the usual answer."* - then create the parent and bring
the system down into it from the address settled in Step 5.

Say one line when it lands. Do not show them the output.

## Step 7 - Hand off, and stop

The moment the system is on the machine, this skill is finished.

> "Your system is on your computer. Everything from here - making it yours, building your
> Business Brain, and putting it to work - is the system's own setup, and it's better at
> that than I am. Starting it now."

Then point Claude at the new folder and start `setup-my-os` from inside it **by saying
what starts it, not by inventing a command for it.** It is a skill that fires on a
phrase, and a made-up slash command or flag is a guess that fails in front of the
student at the finish line. If you are handing off by telling them what to type, the
words are: **set up my OS**.

If they must re-open Claude on that folder first, tell them the one thing they will see:
*"It'll ask whether you trust this folder. Click Trust - that's expected, and it only
asks once."*

Do not re-ask anything `setup-my-os` asks. Do not personalize anything. Stop here.

---

## If she leaves and comes back

She has a job. She will stop mid-way for a showing, a call, or the school run, and come
back an hour or a day later saying some version of *"I'm back, where were we?"*

**Never ask her what was already done.** She does not know, she should not have to know,
and asking is how a person who was doing fine starts to feel like they lost something.
Look at the machine and tell her:

- Are the tools there and do they run?
- Is she signed in?
- Is the system folder there?

Then give her the state in three lines, marking what is done and what is left, and say
plainly how long the rest takes. Lead with what is finished, because the part she is most
likely to dread - the long install - is usually the part already behind her.

Nothing done is ever lost by stopping. Say so.

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
