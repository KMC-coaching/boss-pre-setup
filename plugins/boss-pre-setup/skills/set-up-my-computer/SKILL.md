---
name: set-up-my-computer
description: Primes a brand-new student's computer so it is ready before anything else happens with them, without ever asking them to open a terminal or type a command. Settles what Claude is allowed to do, puts Git and the GitHub tool in place without admin rights, and signs them in to their own GitHub account through their browser. Stops there. Use when the student says "set up my computer", "set me up", "get me started", "prime my machine", "onboard me", "I just joined", or runs this plugin for the first time.
version: 1.7.0
---

# Set Up My Computer

## What this is, and where it stops

This runs on a computer that has nothing on it yet. No GitHub connection, no tools. Its
entire job is to leave the machine **primed**: Git present, the GitHub tool present and
runnable, and the student signed in to their own GitHub account.

That is the whole scope. When the sign-in is confirmed, you are done.

**Their system does not arrive today, and you must not imply that it does.** It comes
later, as a separate step, once they have been given access to it. Nothing in this skill
downloads it, names a folder for it, checks whether they can reach it, or starts its
setup. Do not go looking for it, do not ask what their business is called, and do not
name the system's location or address to them.

**Why this boundary is absolute:** at this moment they have no access to the system, and
that is deliberate. Checking for it would fail, and the failure would look to them like
something they did wrong - a missed invitation, a wrong account - when in fact nothing is
wrong at all. Sending a nervous student hunting through her spam folder for an email that
does not exist yet is the worst outcome this skill can produce. There is nothing to
verify here. Do not verify it.

**If a system folder already exists on this machine,** they are further along than this
skill. Say so in one line and stop; their system has its own setup and it is better at
that than you are.

## The two rules that matter more than the steps

### 1. They never type a command. Not once.

If you are about to say "open your terminal", "paste this", "run this command", or
"create this folder", stop. That sentence is the failure this skill exists to remove. You
have their computer; use it. The only things they do by hand are in Step 4 - the sign-in,
their two-factor codes, and creating a GitHub account if they do not have one - because
no software on earth can do those for them.

### 2. Their words, not yours

Never say: repository, repo, clone, fork, remote, commit, branch, terminal, shell, CLI,
command line, PATH, package manager, Homebrew, sudo, admin rights, token, scope, API,
binary, environment variable.

Their words are: **your system**, **your folder**, **your backup**, **the sign-in**,
**the tool your system will come through**.

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

The only things that are genuinely hers: her own account and password, which GitHub
account she wants her system on, and anything irreversible. Everything else is yours.

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

> "Hi. I'm getting your computer ready. Ten to fifteen minutes, and I do nearly all of
> it. When we're done your machine is set up and ready to go, so that when your system
> comes, everything is already in place for it.
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

1. **Take a copy first** - `settings.json.bak` beside it, **but only if that copy does
   not already exist.** This is the one irreversible thing in the whole skill, and a copy
   costs nothing. Students who have used Claude before may have hooks, connectors and
   permissions in there that took them a long time to get right, and that no one can
   reconstruct for them.

   The "only if it does not already exist" is the whole point, not a detail. This skill
   is built to be re-run after she steps away, and a backup taken unconditionally on a
   second run copies the file you already modified over the only untouched copy of her
   original settings. The safety net silently becomes a second copy of the change. Check
   for the file; if it is there, leave it exactly as it is.
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
(*"Putting the tool in place that your system will come through - about a minute."*).

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

## Step 4 - The two things only they can do

These are the only human steps in the entire install. Do not attempt them yourself, and
do not apologise for them - they exist because they are theirs.

**Before anything else here, ask whether they have a GitHub account.** One plain
question: *"Do you already have a GitHub account?"* If the answer is no, or "I don't
know", go to Step 4a and come back. Do not start the sign-in first and discover it
halfway through - a student staring at a sign-in box for an account that does not exist
will assume she has done something wrong.

**Expect the answer to be no.** Most people in this programme have never had a reason to
use GitHub. That is completely normal and you should say so before she has a chance to
feel behind: *"Most people here don't - it takes a couple of minutes to make one."*

1. **Sign in to GitHub.** Do not improvise this command; it is the one step that is
   awkward to retry, and a wrong scope here fails later with an error that looks like a
   permissions problem instead of a sign-in problem.

   **First check whether they are already signed in.** `gh auth status`. Many students
   are, from something else. If they are signed in but missing scopes, top them up with
   `gh auth refresh` rather than making them sign in again.

   If they are not signed in, run the browser flow **in the background**, never in the
   foreground. Verified on 2026-09-17: inside a tool call there is no terminal attached,
   and this command prints the code and then blocks, polling, until the student finishes
   in their browser. Run in the foreground it looks frozen and eventually times out. Run
   in the background it works exactly as intended.

   Write the output to a fresh temporary file, not a fixed path. A live sign-in code sits
   in this file; a predictable name in a world-readable folder collides between runs and
   between accounts on a shared machine.

   ```
   SIGNIN=$(mktemp -t boss-signin)
   gh auth login --hostname github.com --git-protocol https --web \
     --scopes "repo,read:org,gist,workflow" < /dev/null > "$SIGNIN" 2>&1 &
   ```

   Within a second or two that file holds the code and the address. **Do not pattern-match
   on the exact wording.** It has already changed once and will change again: gh 2.101.0
   (verified 2026-09-17) writes

   ```

   ! One-time code (XXXX-XXXX) copied to clipboard
   Open this URL to continue in your web browser: https://github.com/login/device
   ```

   where an earlier version wrote `! First copy your one-time code: XXXX-XXXX`. Note the
   leading blank line, and the code in parentheses rather than after a colon. Anything
   keyed to one of those two phrasings returns nothing on the other, and it fails at the
   one step where she is the only person who can act.

   **Find the code by its shape, not its label:** the sole `XXXX-XXXX` group of four
   characters, a hyphen, four characters. If you cannot find one, read the file back and
   look at what is actually there rather than guessing or re-running.

   Read the code out and **give it to them with the address, in one message**:

   > "Go to **github.com/login/device** and type in this code: **XXXX-XXXX**
   >
   > Sign in if it asks, approve on your phone if it asks, and come back here. I'll be
   > watching for it - you don't need to tell me when you're done."

   **Current versions also copy the code to her clipboard.** That is usually a help - she
   can paste instead of type - but it silently replaced whatever she had copied. Say it in
   half a sentence if it fits naturally (*"it's on your clipboard too, so you can just
   paste it"*) and never make it a lecture. Do not promise the paste works: you cannot see
   her clipboard, and the older version did not set it.

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

   `repo` is the one that matters - what they will be given access to later is private,
   and without that scope it will not work when it arrives. `read:org` and `gist` are the
   documented minimum alongside it; `workflow` saves a second sign-in later. Remember:
   after a home-folder install, `gh` is not on PATH, so call it by its full path.

   Tell them what is about to happen before it happens: *"A browser tab is opening. Sign
   in to your GitHub account, and approve it on your phone if it asks. Come back here
   when it says you're done."* Then wait. Do not run anything else while that tab is open.

   **Then run `gh auth setup-git`.** This is what lets their machine act as them on GitHub
   later, and it costs nothing now. Skipping it is a common cause of a later step failing
   right after a sign-in that plainly worked.

   **Then confirm which account they landed on, out loud.** Run `gh auth status`, read the
   username back, and ask them to confirm it:

   > "You're signed in as **their-username**. Is that the account you want your system on?"

   This matters more here than it looks. Plenty of people have two GitHub accounts - an
   old personal one and the one they actually use - and the browser signs in as whichever
   was already logged in. Nothing later in this skill can catch a wrong account, so this
   question is the only chance to catch it while it is still free to fix. If it is the
   wrong one, sign out and run the sign-in again rather than carrying on.
2. **Two-factor codes**, whenever their phone asks.

### Step 4a - If they do not have a GitHub account yet

This is the most likely branch in the whole skill, and the one where a nervous person is
most likely to quietly give up. Treat it as a normal part of the path, not an exception.

**This is the one part where she types a lot, and you should say so up front.** Everything
else in this skill was you doing the work. Signing up is her typing an email, a password,
a username, and a code from her inbox. If you do not warn her, the sudden shift from
"I'll handle it" to "now type all this" feels like something went wrong:

> "This bit's all you, I'm afraid - it's your account, so it has to be your typing. Four
> boxes and a code from your email, about two minutes. I'll stay right here and tell you
> what each one wants."

Send her to **https://github.com/signup** and walk her through it one field at a time, at
her pace. Do not paste a list of all four steps at once.

**Never do any of this for her.** Do not open the page and fill it in, do not choose or
type her password, do not enter her email, and do not complete the puzzle. It is her
account and her credentials, and this is a hard line, not a preference.

What to tell her, in order, each one *before* she hits it:

- **Email.** Recommend the address she will still have in five years - a personal one, or
  her own business domain. A brokerage address stops working the day she changes
  brokerages, and this account outlives that. State it as a recommendation and take
  whatever she picks.
- **Password.** She makes it up, she keeps it. Say plainly, once and without drama:
  *"Don't type it here - I don't need it and I shouldn't see it."* A nervous person's
  instinct is to show you everything she is doing. If she pastes it into the chat anyway,
  do not repeat it back, do not store it, and tell her calmly to change it.
- **Username.** This is the one that matters later, because it is what goes on the form at
  the end and it is how her access gets set up. Recommend her name or her business name,
  something she would be happy to have seen. It is awkward to change afterwards. If she
  asks you to pick, pick one from her name and move on.
- **The email code.** GitHub sends a code to the address she just used. She switches to
  her inbox, gets it, comes back. Tell her it is coming *before* she goes looking, and
  tell her to check spam if it has not shown up in a minute. This is a common place to
  get lost, because leaving the page feels like abandoning the setup. It is not, and say
  so.
- **The puzzle.** GitHub may ask her to solve a small visual or audio puzzle to prove she
  is a person. **You cannot do this one and must not try.** Warn her it is coming so it
  does not read as a failure, tell her there is an audio option if the pictures are hard
  to make out, and tell her plainly that getting it wrong costs nothing - it just gives
  her another.
- **Two-factor.** GitHub will very likely ask her to set up a second security step, either
  straight away or shortly after. This needs her phone. If her phone is not with her, say
  so now rather than when she is halfway in: it is worth pausing two minutes to go and get
  it, and nothing done so far is lost by waiting.

When the account exists, come straight back and run the sign-in. She is already signed in
to GitHub in her browser at that point, so the sign-in usually goes through in seconds.

**One thing to watch.** If she already had a different GitHub account logged in to that
browser, the sign-in may bind to the old one rather than the new. That is exactly what the
username confirmation at the end of the sign-in is for - read it back and make sure it is
the account she just created.

## Step 5 - Hand them their username and the form, and stop

The machine is primed. There is one thing left, and it is the thing that gets their
system to them: **their GitHub username has to reach us, so they can be given access.**
Without it nothing else can happen, so this is not a footnote at the end - it is the
point of the whole session.

Read the username back off `gh auth status` rather than asking them for it. They have
just confirmed it in Step 4, they may not remember it, and a typo here is what stalls
their access for days.

> "You're all set - your computer's ready.
>
> One last thing, and it's the important one. Your GitHub username is:
>
> **their-username**
>
> Fill that into this form so we can get your system over to you:
>
> https://app.kristamashore.com/widget/form/YKntnvJemn7AtAqVY5f9
>
> That's everything. Once that's in, your system comes next and I'll take it from there."

Three rules for this message:

- **Give them the username. Do not ask for it.** They are being asked to type it into a
  form; your job is to make sure the thing they type is right.
- **Give the address as a plain link and do not open it for them.** It is their form to
  fill in, in their own browser, with their own details. Never fill it in on their behalf
  and never enter anything of theirs into it.
- **Do not put a date on what happens next.** You do not know when their access lands.
  "Your system comes next" is true. "In a few days" is a guess, and a guess here turns
  into a support question when it slips.

Then stop. Do not go looking for their system, do not offer to install anything else, and
do not start another setup. If they ask what happens now, the honest answer is that their
access gets set up on our side once the form is in, and everything after that has its own
walkthrough when it arrives.

---

## If she leaves and comes back

She has a job. She will stop mid-way for a showing, a call, or the school run, and come
back an hour or a day later saying some version of *"I'm back, where were we?"*

**Never ask her what was already done.** She does not know, she should not have to know,
and asking is how a person who was doing fine starts to feel like they lost something.
Look at the machine and tell her:

- Are the tools there and do they run?
- Is she signed in, and as which account?
- Has she been given her username and the form?

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
- Never create a GitHub account for them, type their password or email into a signup
  form, or complete a human-verification puzzle on their behalf.
- Never take a backup over a backup that already exists.
- Never go looking for their operating system, check whether they can reach it, download
  it, name a folder for it, or say where it lives. They have no access to it yet, by
  design, and a failed check reads to them as their own mistake.
- Never ask what their business is called in order to name a folder or a system. Nothing
  here needs it. (Suggesting it as a shape for their own GitHub username is fine - that is
  theirs, and they volunteer it or they don't.)
- Never put a date on when their system arrives.
- Never fill in the form for them, or enter any of their details into it.
- Never continue past Step 5 into work that belongs to their system's own setup.
