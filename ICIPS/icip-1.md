---
icip: 1
title: ICIP Purpose and Guidelines
author: 2infiniti <2infiniti@gmail.com>
discussions-to: https://github.com/hx57/ICIPs/issues/
status: Active    
type: Meta
created: 2018-07-23
---

## What is an ICIP?

ICIP stands for ICON Community Improvement Proposal. An ICIP is a design document providing information to the ICON community, or describing new initiatives driven by the ICON Community Alliance (hx57). The ICIP should provide a concise action plans and a solid rationale behind these actions. The ICIP author is responsible for building consensus within the community and documenting dissenting opinions.

## ICIP Rationale

We intend ICIPs to be the primary mechanisms for proposing new community initiatives, for collecting community input on an issue, and for documenting the design decisions that have gone into ICON Community Alliance. Because the ICIPs are maintained as text files in a versioned repository, their revision history is the historical record of the initiative proposal.

For ICON Community Alliance members, ICIPs are a convenient way to track the progress of current implementations. Ideally each implementation maintainer would list the ICIPs that they have implemented. This will give end users a convenient way to know the current status of a given implementation.

# ICIP Type
* **Community** - only community resources required
* **Hybrid** - will require some of team's help to some extent
* **Team** - proposed for team's evaluation

## ICIP Work Flow

Parties involved in the process are you, the champion or *ICIP author*, the [*ICIP editors*](#ICIP-editors), and the [*ICON Core Developers*](https://github.com/icon-project/pm).

:warning: Before you begin, vet your idea, this will save you time. Ask the ICON community first if an idea is original to avoid wasting time on something that will be be rejected based on prior research (searching the Internet does not always do the trick). It also helps to make sure the idea is applicable to the entire community and not just the author. Just because an idea sounds good to the author does not mean it will work for most people in most areas where ICON is used. Examples of appropriate public forums to gauge interest around your ICIP include [the ICON subreddit](https://www.reddit.com/r/helloicon/), and [the Issues section of this repository](https://github.com/icon-project/ICIPs/issues). In particular, [the Issues section of this repository](https://github.com/icon-project/ICIPs/issues) is an excellent place to discuss your proposal with the community and start creating more formalized language around your ICIP.

Your role as the champion is to write the ICIP using the style and format described below, shepherd the discussions in the appropriate forums, and build community consensus around the idea. Following is the process that a successful ICIP will move along:

```
[ WIP ] -> [ DRAFT ] -> [ LAST CALL ] -> [ ACCEPTED ] -> [ FINAL ]
```

Each status change is requested by the ICIP author and reviewed by the ICIP editors. Use a pull request to update the status. Please include a link to where people should continue discussing your ICIP. The ICIP editors will process these requests as per the conditions below.

* **Work in progress (WIP)** -- Once the champion has asked the ICON community whether an idea has any chance of support, they will write a draft ICIP as a [pull request](https://github.com/icon-project/ICIPs/pulls). Consider including an implementation if this will aid people in studying the ICIP.
  * :arrow_right: Draft -- If agreeable, ICIP editor will assign the ICIP a number (generally the issue or PR number related to the ICIP) and merge your pull request. The ICIP editor will not unreasonably deny an ICIP.
  * :x: -- Reasons for denying draft status include being too unfocused, too broad, duplication of effort, being technically unsound, not providing proper motivation or addressing backwards compatibility, or not in keeping with the ICON vision.
* **Draft** -- Once the first draft has been merged, you may submit follow-up pull requests with further changes to your draft until such point as you believe the ICIP to be mature and ready to proceed to the next status. An ICIP in draft status must be implemented to be considered for promotion to the next status (ignore this requirement for core ICIPs).
  * :arrow_right: Last Call -- If agreeable, the ICIP editor will assign Last Call status and set a review end date, normally 14 days later.
  * :x: -- A request for Last Call status will be denied if material changes are still expected to be made to the draft. We hope that ICIPs only enter Last Call once, so as to avoid unnecessary noise on the RSS feed. Last Call will be denied if the implementation is not complete and supported by the community.
* **Last Call** -- This ICIP will listed prominently on the https://github.com/icon-project/ICIPs.  
  * :x: -- A Last Call which results in material changes or substantial unaddressed complaints will cause the ICIP to revert to Draft.
  * :arrow_right: Accepted (Core ICIPs only) -- After the review end date, the ICON Core Developers will vote on whether to accept this change. If yes, the status will upgrade to Accepted.
  * :arrow_right: Final (Not core ICIPs) -- A successful Last Call without material changes or unaddressed complaints will become Final.
* **Accepted (Core ICIPs only)** -- This is being implemented by ICON Core Developers.
  * :arrow_right: Final -- Standards Track Core ICIPs must be implemented in at least three viable ICON clients before it can be considered Final. When the implementation is complete and supported by the community, the status will be changed to “Final”.
* **Final** -- This ICIP represents the current state-of-the-art. A Final ICIP should only be updated to correct errata.

Other exceptional statuses include:

* Deferred -- This is for core ICIPs that have been put off for a future release.
* Rejected -- An ICIP that is fundamentally broken and will not be implemented.
* Active -- This is similar to Final, but denotes an ICIP which may be updated without changing its ICIP number.
* Superseded -- An ICIP which was previously final but is no longer considered state-of-the-art. Another ICIP will be in Final status and reference the Superseded ICIP.

## What belongs in a successful ICIP?

Each ICIP should have the following parts:

- Preamble - RFC 822 style headers containing metadata about the ICIP, including the ICIP number, a short descriptive title (limited to a maximum of 44 characters), and the author details. See [below](https://github.com/icon-project/ICIPs/blob/master/ICIPS/ICIP-1.md#ICIP-header-preamble) for details.
- Simple Summary - “If you can’t explain it simply, you don’t understand it well enough.” Provide a simplified and layman-accessible explanation of the ICIP.
- Abstract - a short (~200 word) description of the technical issue being addressed.
- Motivation (*optional) - The motivation is critical for ICIPs that want to change the ICON protocol. It should clearly explain why the existing protocol specification is inadequate to address the problem that the ICIP solves. ICIP submissions without sufficient motivation may be rejected outright.
- Specification - The technical specification should describe the syntax and semantics of any new feature. The specification should be detailed enough to allow competing, interoperable implementations for any of the current ICON platforms.
- Rationale - The rationale fleshes out the specification by describing what motivated the design and why particular design decisions were made. It should describe alternate designs that were considered and related work, e.g. how the feature is supported in other languages. The rationale may also provide evidence of consensus within the community, and should discuss important objections or concerns raised during discussion.
- Backwards Compatibility - All ICIPs that introduce backwards incompatibilities must include a section describing these incompatibilities and their severity. The ICIP must explain how the author proposes to deal with these incompatibilities. ICIP submissions without a sufficient backwards compatibility treatise may be rejected outright.
- Test Cases - Test cases for an implementation are mandatory for ICIPs that are affecting consensus changes. Other ICIPs can choose to include links to test cases if applicable.
- Implementations - The implementations must be completed before any ICIP is given status “Final”, but it need not be completed before the ICIP is merged as draft. While there is merit to the approach of reaching consensus on the specification and rationale before writing code, the principle of “rough consensus and running code” is still useful when it comes to resolving many discussions of API details.
- Copyright Waiver - All ICIPs must be in the public domain. See the bottom of this ICIP for an example copyright waiver.

## ICIP Formats and Templates

ICIPs should be written in [markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) format.
Image files should be included in a subdirectory of the `assets` folder for that ICIP as follow: `assets/ICIP-X` (for ICIP **X**). When linking to an image in the ICIP, use relative links such as `../assets/ICIP-X/image.png`.

## ICIP Header Preamble

Each ICIP must begin with an RFC 822 style header preamble, preceded and followed by three hyphens (`---`). The headers must appear in the following order. Headers marked with "*" are optional and are described below. All other headers are required.

` icip:` <ICIP number> (this is determined by the ICIP editor)

` title:` <ICIP title>

` author:` <a list of the author's or authors' name(s) and/or username(s), or name(s) and email(s). Details are below.>

` * discussions-to:` <url>

` status:` <Draft | Last Call | Accepted | Final | Active | Deferred | Rejected | Superseded>

`* review-period-end`: YYYY-MM-DD

` type: `<Standards Track (Core, Networking, Interface, IRC)  | Informational | Meta>

` * category:` <Core | Networking | Interface | IRC>

` created:` <date created on, in ISO 8601 (yyyy-mm-dd) format>

` * requires:` <ICIP number(s)>

` * replaces:` <ICIP number(s)>

` * superseded-by:` <ICIP number(s)>

` * resolution:` <url>

##### author header

The `author` header optionally lists the names, email addresses or usernames of the authors/owners of the ICIP. Those who prefer anonymity may use a username only, or a first name and a username. The format of the author header value must be:

Random J. User &lt;address@dom.ain&gt;

or

Random J. User (@username)

if the email address or GitHub username is included, and

Random J. User

if the email address is not given.

##### resolution header

Note: The `resolution` header is required for Standards Track ICIPs only. It contains a URL that should point to an email message or other web resource where the pronouncement about the ICIP is made.

##### discussions-to header

While an ICIP is a draft, a `discussions-to` header will indicate the mailing list or URL where the ICIP is being discussed. As mentioned above, examples for places to discuss your ICIP include an issue in this repo or in a fork of this repo, and [Reddit r/helloicon](https://www.reddit.com/r/helloicon/). No discussions-to header is necessary if the ICIP is being discussed privately with the author.

##### type header

The `type` header specifies the type of ICIP: Standards Track, Meta, or Informational. If the track is Standards please include the subcategory (core, networking, interface, or IRC).

##### category header

The `category` header specifies the ICIP's category. This is required for standards-track ICIPs only.

##### created header

The `created` header records the date that the ICIP was assigned a number. Both headers should be in yyyy-mm-dd format, e.g. 2018-08-15.

##### requires header

ICIPs may have a `requires` header, indicating the ICIP numbers that this ICIP depends on.

##### superseded-by header

ICIPs may also have a `superseded-by` header indicating that an ICIP has been rendered obsolete by a later document; the value is the number of the ICIP that replaces the current document. The newer ICIP must have a `replaces` header containing the number of the ICIP that it rendered obsolete.

Headers that permit lists must separate elements with commas.

## Auxiliary Files

ICIPs may include auxiliary files such as diagrams. Such files must be named ICIP-XXXX-Y.ext, where “XXXX” is the ICIP number, “Y” is a serial number (starting at 1), and “ext” is replaced by the actual file extension (e.g. “png”).

## Transferring ICIP Ownership

It occasionally becomes necessary to transfer ownership of ICIPs to a new champion. In general, we'd like to retain the original author as a co-author of the transferred ICIP, but that's really up to the original author. A good reason to transfer ownership is because the original author no longer has the time or interest in updating it or following through with the ICIP process, or has fallen off the face of the 'net (i.e. is unreachable or isn't responding to email). A bad reason to transfer ownership is because you don't agree with the direction of the ICIP. We try to build consensus around an ICIP, but if that's not possible, you can always submit a competing ICIP.

If you are interested in assuming ownership of an ICIP, send a message asking to take over, addressed to both the original author and the ICIP editor. If the original author doesn't respond to email in a timely manner, the ICIP editor will make a unilateral decision (it's not like such decisions can't be reversed :)).

## ICIP Editors

The current ICIP editors are

`* Jonghyup Kim (@extendjh)`

`* Sojin Kim (@sojinkim-icon)`

`* Jaechang Namgoong (@sink772)`

## ICIP Editor Responsibilities

For each new ICIP that comes in, an editor does the following:

- Read the ICIP to check if it is ready: sound and complete. The ideas must make technical sense, even if they don't seem likely to get to final status.
- The title should accurately describe the content.
- Check the ICIP for language (spelling, grammar, sentence structure, etc.), markup (Github flavored Markdown), code style

If the ICIP isn't ready, the editor will send it back to the author for revision, with specific instructions.

Once the ICIP is ready for the repository, the ICIP editor will:

- Assign an ICIP number (generally the PR number or, if preferred by the author, the Issue # if there was discussion in the Issues section of this repository about this ICIP)

- Merge the corresponding pull request

- Send a message back to the ICIP author with the next step.

Many ICIPs are written and maintained by developers with write access to the ICON codebase. The ICIP editors monitor ICIP changes, and correct any structure, grammar, spelling, or markup mistakes we see.

The editors don't pass judgment on ICIPs. We merely do the administrative & editorial part.

## History

This document was derived heavily from [Ethereum's EIP-1](https://github.com/ethereum/EIPs) which in turn was derived from [Bitcoin's BIP-0001](https://github.com/bitcoin/bips) and [Python's PEP-0001](https://www.python.org/dev/peps/). In many places text was simply copied and modified. Authors of EIP-1, BIP-0001, and PEP-0001 are not responsible for its use in the ICON Improvement Process, and should not be bothered with technical questions specific to ICON or the ICIP. Please direct all comments to the ICIP editors.

July 29, 2018: ICIP 1 has been improved and placed as a PR.

Auguest 1, 2018: Merged to master. 

## Copyright

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).