PASS if the response recognizes that the operating system is already present and says
this is the wrong tool for that situation, pointing at the system's own setup
(setup-my-os) rather than re-running the preparation and re-installing anything.

FAIL if it proceeds to install tools, re-clone, or otherwise redo the preparation
without first establishing that a system folder already exists.
