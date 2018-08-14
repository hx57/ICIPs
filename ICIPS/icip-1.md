---
icip: 1
title: ICIP Purpose and Guidelines
author: 2infiniti <2infiniti@gmail.com>
discussions-to: https://github.com/hx57/ICIPs/issues/1
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

##### discussions-to header

While an ICIP is a draft, a `discussions-to` header will indicate the mailing list or URL where the ICIP is being discussed. As mentioned above, examples for places to discuss your ICIP include an issue in this repo or in a fork of this repo, and [ICON Community Alliance HX57](https://t.me/iconhx57). No discussions-to header is necessary if the ICIP is being discussed privately with the author.

##### type header

The `type` header specifies the type of ICIP

##### category header

The `category` header specifies the ICIP's category.

##### created header

The `created` header records the date that the ICIP was assigned a number. Both headers should be in yyyy-mm-dd format, e.g. 2018-08-15.

##### requires header

ICIPs may have a `requires` header, indicating the ICIP numbers that this ICIP depends on.

##### superseded-by header

ICIPs may also have a `superseded-by` header indicating that an ICIP has been rendered obsolete by a later document; the value is the number of the ICIP that replaces the current document. The newer ICIP must have a `replaces` header containing the number of the ICIP that it rendered obsolete.

Headers that permit lists must separate elements with commas.

## ICIP Editors

The current ICIP editors are

`* 2infiniti (@msg2infiniti)`


## ICIP Editor Responsibilities

For each new ICIP that comes in, an editor does the following:

- Read the ICIP to check if it is ready: sound and complete. The ideas must make sense, even if they don't seem likely to get to final status.
- The title should accurately describe the content.
- Check the ICIP for language (spelling, grammar, sentence structure, etc.), markup (Github flavored Markdown), code style

If the ICIP isn't ready, the editor will send it back to the author for revision, with specific instructions.

Once the ICIP is ready for the repository, the ICIP editor will:

- Assign an ICIP number (generally the PR number or, if preferred by the author, the Issue # if there was discussion in the Issues section of this repository about this ICIP)

- Merge the corresponding pull request

- Send a message back to the ICIP author with the next step.

The editors don't pass judgment on ICIPs. We merely do the administrative & editorial part.

## History

This document was derived heavily from [icon-project's EIP-1](https://github.com/icon-project/IIPs/blob/master/IIPS/iip-1.md). In many places text was simply copied and modified. Authors of icon-project EIP-1 are not responsible for its use in the ICON Community Improvement Process, and should not be bothered with questions specific to ICON Community Alliance or the ICIP. Please direct all comments to the ICIP editors.


## Copyright

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).