## Configuration Management to Encourage Collaboration and Avoid Repetition

Phil Fenstermacher

pcfens@wm.edu

---

## Who am I?

Systems Engineer for ~6 years

Fan of automation and old keyboards <!-- .element: class="fragment" -->

---

## Configuration Management
* A tool to manage and enforce server/software configurations
* Popular options include Chef, Salt, Ansible, and Puppet (we use Puppet).
* For the sake of this discussion, they're kept in code <!-- .element: class="fragment" -->

---

![Model M](keyboard.jpg "Model M")
The only clicky-clicky that goes on

---

## Collaboration
Working across traditional silos (e.g. Banner Software Team and operations)

Note:
Next piece is discuss why we need these things

---

## Configuration Management
Keeping configuration in code lets us:
* keep it in SCM
* test it
* roll back when I break something

Note: Testing is important because it lets you move faster with greater confidence

---

## Collaboration/Shared Risks

* Shared risks reduce overall risks
* Fewer issues
* Faster recovery from issues

Note: State of devops report is an interesting read on how IT performance can be
measured in terms of these things

---

## Repetition
* It's boring: when people get bored they start to make mistakes
* Time spent not solving problems you still have

Note:
* Computers are good at repeating things without fatigue

* Banner web tier machines were set up manually, supposedly identically,
but they were different, one was broken, and nobody knew why

---

## On the ops team
* Configuration Management data is kept in git
* On a push to git, tests are run
* If tests pass, the new config is deployed to our puppet server for enforcement
* Failure is announced in the group chat

---

## On other teams
* A change is proposed using a git merge request
* Operations looks at the code to see if it should be merged
* Tests are run on the MR
* Merged code that passes tests are deployed automatically

---

## Testing
* Static analysis
* Unit/Spec Testing
* Acceptance Testing

Note: Useful for collaborating with untrusted groups

---

## Static Analysis

* File/folder structure
* Basic Syntax
* Style/Lint Checking

---

## Unit/Spec Testing

* Test output with a known input
* Catches logic errors in complex situations

Note: Compiles everything - useful for upgrade testing

---

## Acceptance Testing

* Apply configuration to a machine/container and test for success

Note: What beyond ability to collaborate safely?

---

## Other Gains

* Backup data only, not full systems
* Copy paste infrastructure
* Writing documentation == configuring servers <!-- .element: class="fragment" -->

Note: Discuss the piece running in AWS

---

## Everything in git

* VM Templates are built using packer
* Documentation lives with the code

Note: Docs must be markdown or plaintext - viewable in vi is a must

---

## Getting Here

* 5 Years
* Small Goals <!-- .element: class="fragment" -->
* Build the Culture <!-- .element: class="fragment" -->

Note: Tooling has come a long way, much easier to do full testing today

---

## What Next?

* Device/Appliance Configuration
* Existence of resources
* Running containers

---

[github.com/pcfens/mabug2016](https://github.com/pcfens/mabug2016)

---
## Demo Time
