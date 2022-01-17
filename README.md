# What is This Repository?
This repository is a list of situations that occur in bug bounty programs and how they should be handled. Many of these are currently handled on a case-by-case basis, which leads to a lot of uncertainty and frustration from hackers, program owners and platforms. The goal of this repository is to standardise the way that these edge-cases are handled across all bounty platforms and programs. Hopefully standardization will allow expectations to be fulfilled more frequently from all parties.


# This is a Draft

This document is a draft, and not yet implemented by any bug bounty platforms. At this stage, I am requesting comments from all interested parties.

# How to Contribute

Please contribute by opening GitHub issues. All reasonable issues submitted will remain open for a minimum of 30 days for comments.

Your issue should state an opinion, e.g.

- I feel that a scenario should be added for when a hacker reaches out directly to the program directly instead of reporting through the provided platform.
- I feel that a scenario should be added for one party is abusive to another.
- I feel that the resolution for scenario 4 should be changed to "hacker is able to publicly disclose vulnerability after 120 days of non-response".

Comments on the issue are welcome by anyone, but must be constructive and unemotional. Abusive behaviour will not be tolerated.

# The Table


| ID | Situation                                                                                                                                                                                                                                                                            | Resolution                                                                                                                                                                                                                                                                                  |
| -- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1  | Hacker submits vulnerability with proof of exploitation. The vulnerability is fixed before the submission is triaged.                                                                                                                                                                | Platform must provide proof that the submission was not accessed by the program prior to resolution. If the submission was accessed by the program, the program should pay the relevant bounty, otherwise submission is marked as duplicate.                                                |
| 2  | Hacker submits vulnerability, program responds saying that they already knew about it internally.                                                                                                                                                                                    | Program must provide proof that this was a previously known issue, for example, a screenshot of a Jira ticket including the date created. If the program is unable to provide proof, they should pay the bounty, otherwise the submission should be marked as a duplicate.                  |
| 3  | Hacker submits vulnerability, it is marked as a duplicate of another submission that did not fully explore the impact of the bug. For example, a hacker submits a full XSS which allows an account takeover, and dupes against another submission that only reported HTML injection. | The first reporter receives a bounty based on the impact of their submission, the second reporter receives a bounty based on the impact of their submission minus the bounty received by the first reporter.                                                                                |
| 4  | Hacker submits vulnerability, the program never responds.                                                                                                                                                                                                                            | Platform pays the bounty.                                                                                                                                                                                                                                                                   |
| 5  | Hacker submits vulnerability, hacker is incorrectly duped against a newer report.                                                                                                                                                                                                    | Platform changes the status of both reports to be accurate. If payment has already been made incorrectly, the organization who triaged incorrectly pays the bounty. For managed bounty programs this would generally be the platform, but for unmanaged programs this would be the program. |
| 6  | Hacker disagrees on the assigned severity rating.                                                                                                                                                                                                                                    | Hacker submits reasoning to ticket. If there is no response for 14 days, hacker submits reasoning to the platform's support channel. Severity upgrades are decided on a per-submission basis.                                                                                               |
| 7  | Hacker publicly discloses a bug that has been previously submitted to the platform, without explicit permission from the program owner.                                                                                                                                              | Hacker receives 30 day ban from platform, hacker is emailed with full reasoning behind ban. Repeat offence results in permanent ban.                                                                                                                                                        |
| 8  | Hacker submits a bug that is within scope of the program, but is actually a bug in a third-party service.                                                                                                                                                                            | Every program should specify whether they accept bugs on 3rd party systems within their brief. If there is no specification, then it is assumed that ALL systems listed in the scope will be accepted for vulnerabilities, including 3rd party systems.                                     |
