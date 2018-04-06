    MIP: 1
      Title: MIP Purpose and Guidelines
      Status: Draft
      Type: Meta
      Author: Hao Chen<hao.chen@mvs.org>
      Created: 2017-06-01

What is an MIP?
--------------

MIP stands for Metaverse Improvement Proposal. An MIP is a design document providing information to the Metaverse community, or describing a new feature for Metaverse or its processes or environment. The MIP should provide a concise technical specification of the feature and a rationale for the feature. The MIP author is responsible for building consensus within the community and documenting dissenting opinions.

MIP Rational
------------

We intend MIPs to be the primary mechanisms for proposing new features, for collecting community input on an issue, and for documenting the design decisions that have gone into Metaverse. Because the MIPs are maintained as text files in a versioned repository, their revision history is the historical record of the feature proposal.

For Metaverse implementers, MIPs are a convenient way to track the progress of their implementation. Ideally each implementation maintainer would list the MIPs that they have implemented. This will give end users a convenient way to know the current status of a given implementation or library.

MIP Types
---------

There are three types of MIP:

-   A **Standard Track MIP** describes any change that affects most or all Metaverse implementations, such as a change to the the network protocol, a change in block or transaction validity rules, proposed application standards/conventions, or any change or addition that affects the interoperability of applications using Metaverse. Furthermore Standard MIPs can be broken down into the following categories.
    -   **Core** - improvements requiring a consensus fork (e.g. [MIP02]]), as well as changes that are not necessarily consensus critical but may be relevant to “core dev” discussions.
    -   **Networking** - includes improvements around, as well as proposed improvements to network protocol.
    -   **Interface** - includes improvements around client [API/RPC] specifications and standards, and also certain language-level standards like method names . The label “interface” aligns with the [interfaces repo] and discussion should primarily occur in that repository before an MIP is submitted to the MIPs repository.
    -   **ECO** - economy-level standards and conventions, including token usage standards such as digital asset standards (**[MST] Metaverse Smart Token**), digital identity standards (**[MID] Metaverse Didigtal Identity**).

-   An **Informational MIP** describes a Metaverse design issue, or provides general guidelines or information to the Metaverse community, but does not propose a new feature. Informational MIPs do not necessarily represent Metaverse community consensus or a recommendation, so users and implementers are free to ignore Informational MIPs or follow their advice.
-   A **Meta MIP** (MMIP) describes a process surrounding Metaverse or proposes a change to (or an event in) a process. Process MIPs are like Standards Track MIPs but apply to areas other than the Metaverse protocol itself. They may propose an implementation, but not to Metaverse's codebase; they often require community consensus; unlike Informational MIPs, they are more than recommendations, and users are typically not free to ignore them. Examples include procedures, guidelines, changes to the decision-making process, and changes to the tools or environment used in Metaverse development. Any meta-MIP is also considered a Process MIP.

MIP Work Flow
-------------

The MIP repository Collaborators change the MIPs status. Please send all MIP-related email to the MIP Collaborators, which is listed under MIP Editors below. Also see MIP Editor Responsibilities & Workflow.

The MIP process begins with a new idea for Metaverse. It is highly recommended that a single MIP contain a single key proposal or new idea. The more focused the MIP, the more successful it tends to be. A change to one client doesn't require an MIP; a change that affects multiple clients, or defines a standard for multiple apps to use, does. The MIP editor reserves the right to reject MIP proposals if they appear too unfocused or too broad. If in doubt, split your MIP into several well-focused ones.

Each MIP must have a champion - someone who writes the MIP using the style and format described below, shepherds the discussions in the appropriate forums, and attempts to build community consensus around the idea.

Vetting an idea publicly before going as far as writing an MIP is meant to save the potential author time. Asking the Metaverse community first if an idea is original helps prevent too much time being spent on something that is guaranteed to be rejected based on prior discussions (searching the Internet does not always do the trick). It also helps to make sure the idea is applicable to the entire community and not just the author. Just because an idea sounds good to the author does not mean it will work for most people in most areas where Metaverse is used. Examples of appropriate public forums to gauge interest around your MIP include [the Metaverse subreddit], [the Issues section of this repository], and [one of the Metaverse Gitter chat rooms]. In particular, [the Issues section of this repository] is an excellent place to discuss your proposal with the community and start creating more formalized language around your MIP. 

Once the champion has asked the Metaverse community whether an idea has any chance of acceptance a draft MIP should be presented as a [pull request]. This gives the author a chance to continuously edit the draft MIP for proper formatting and quality. This also allows for further public comment and the author of the MIP to address concerns about the proposal.

If the MIP collaborators approve, the MIP editor will assign the MIP a number (generally the issue or PR number related to the MIP), label it as Standards Track, Informational, or Meta, give it status “Draft”, and add it to the git repository. The MIP editor will not unreasonably deny an MIP. Reasons for denying MIP status include duplication of effort, being technically unsound, not providing proper motivation or addressing backwards compatibility, or not in keeping with the Metaverse philosophy.

Standards Track MIPs consist of three parts, a design document, implementation, and finally if warranted an update to the [formal specification]. The MIP should be reviewed and accepted before an implementation is begun, unless an implementation will aid people in studying the MIP. Standards Track MIPs must be implemented in at least three viable Metaverse clients before it can be considered Final.

For an MIP to be accepted it must meet certain minimum criteria. It must be a clear and complete description of the proposed enhancement. The enhancement must represent a net improvement. The proposed implementation, if applicable, must be solid and must not complicate the protocol unduly.

Once an MIP has been accepted, the implementations must be completed. When the implementation is complete and accepted by the community, the status will be changed to “Final”.

An MIP can also be assigned status “Deferred”. The MIP author or editor can assign the MIP this status when no progress is being made on the MIP. Once an MIP is deferred, the MIP editor can re-assign it to draft status.

An MIP can also be “Rejected”. Perhaps after all is said and done it was not a good idea. It is still important to have a record of this fact.

MIPs can also be superseded by a different MIP, rendering the original obsolete.

The possible paths of the status of MIPs are as follows:

<img src=./MMIP-1/process.png>

Some Informational and Process MIPs may also have a status of “Active” if they are never meant to be completed. E.g. MIP 1 (this MIP).

What belongs in a successful MIP?
---------------------------------

Each MIP should have the following parts:

-   Preamble - RFC 822 style headers containing metadata about the MIP, including the MIP number, a short descriptive title (limited to a maximum of 44 characters), the names, and optionally the contact info for each author, etc.

<!-- -->

-   Simple Summary - “If you can’t explain it simply, you don’t understand it well enough.” Provide a simplified and layman-accessible explanation of the MIP.

<!-- -->

-   Abstract - a short (~200 word) description of the technical issue being addressed.

<!-- -->

-   Motivation (*optional) - The motivation is critical for MIPs that want to change the Metaverse protocol. It should clearly explain why the existing protocol specification is inadequate to address the problem that the MIP solves. MIP submissions without sufficient motivation may be rejected outright.

<!-- -->

-   Specification - The technical specification should describe the syntax and semantics of any new feature. The specification should be detailed enough to allow competing, interoperable implementations for any of the current Metaverse platforms (cpp-Metaverse, go-Metaverse, parity, MetaverseJ, Metaversejs-lib, …).

<!-- -->

-   Rationale - The rationale fleshes out the specification by describing what motivated the design and why particular design decisions were made. It should describe alternate designs that were considered and related work, e.g. how the feature is supported in other languages. The rationale may also provide evidence of consensus within the community, and should discuss important objections or concerns raised during discussion.

<!-- -->

-   Backwards Compatibility - All MIPs that introduce backwards incompatibilities must include a section describing these incompatibilities and their severity. The MIP must explain how the author proposes to deal with these incompatibilities. MIP submissions without a sufficient backwards compatibility treatise may be rejected outright.

<!-- -->

-   Test Cases - Test cases for an implementation are mandatory for MIPs that are affecting consensus changes. Other MIPs can choose to include links to test cases if applicable.

<!-- -->

-   Implementations - The implementations must be completed before any MIP is given status “Final”, but it need not be completed before the MIP is accepted. While there is merit to the approach of reaching consensus on the specification and rationale before writing code, the principle of “rough consensus and running code” is still useful when it comes to resolving many discussions of API details.

MIP Formats and Templates
-------------------------

MIPs should be written in [markdown] format. Image files should be included in a subdirectory for that MIP.

MIP Header Preamble
-------------------

Each MIP must begin with an RFC 822 style header preamble. The headers must appear in the following order. Headers marked with "*" are optional and are described below. All other headers are required.

` MIP: ` <MIP number> (this is determined by the MIP editor)

` Title: `<MIP title>

` Author: `<list of author's real names and optionally, email address>

` * Discussions-To: ` <email address>

` Status: `<Draft | Active | Accepted | Deferred | Rejected | Withdrawn | Final | Superseded>

` Type: `<Standards Track (Core, Networking, Interface, ERC)  | Informational | Process>

` Created: `<date created on, in ISO 8601 (yyyy-mm-dd) format>

` * Replaces: `<MIP number>

` * Superseded-By: `<MIP number>

` * Resolution: `<url>

The Author header lists the names, and optionally the email addresses of all the authors/owners of the MIP. The format of the Author header value must be

Random J. User &lt;address@dom.ain&gt;

if the email address is included, and

Random J. User

if the email address is not given.

Note: The Resolution header is required for Standards Track MIPs only. It contains a URL that should point to an email message or other web resource where the pronouncement about the MIP is made.

While an MIP is in private discussions (usually during the initial Draft phase), a Discussions-To header will indicate the mailing list or URL where the MIP is being discussed. No Discussions-To header is necessary if the MIP is being discussed privately with the author.

The Type header specifies the type of MIP: Standards Track, Meta, or Informational. If the track is Standards please include the subcategory (core, networking, interface, or ERC).

The Created header records the date that the MIP was assigned a number. Both headers should be in yyyy-mm-dd format, e.g. 2001-08-14.

MIPs may have a Requires header, indicating the MIP numbers that this MIP depends on.

MIPs may also have a Superseded-By header indicating that an MIP has been rendered obsolete by a later document; the value is the number of the MIP that replaces the current document. The newer MIP must have a Replaces header containing the number of the MIP that it rendered obsolete.

Auxiliary Files
---------------

MIPs may include auxiliary files such as diagrams. Such files must be named MIP-XXXX-Y.ext, where “XXXX” is the MIP number, “Y” is a serial number (starting at 1), and “ext” is replaced by the actual file extension (e.g. “png”).

Transferring MIP Ownership
--------------------------

It occasionally becomes necessary to transfer ownership of MIPs to a new champion. In general, we'd like to retain the original author as a co-author of the transferred MIP, but that's really up to the original author. A good reason to transfer ownership is because the original author no longer has the time or interest in updating it or following through with the MIP process, or has fallen off the face of the 'net (i.e. is unreachable or not responding to email). A bad reason to transfer ownership is because you don't agree with the direction of the MIP. We try to build consensus around an MIP, but if that's not possible, you can always submit a competing MIP.

If you are interested in assuming ownership of an MIP, send a message asking to take over, addressed to both the original author and the MIP editor. If the original author doesn't respond to email in a timely manner, the MIP editor will make a unilateral decision (it's not like such decisions can't be reversed :).

MIP Editors
-----------

The current MIP editors are

` * Youming Jiang(@Youming)`

` * Eirc Gu(@Eric)`

` * Hao Chen(@Hao)`

MIP Editor Responsibilities and Workflow
--------------------------------------

For each new MIP that comes in, an editor does the following:

-   Read the MIP to check if it is ready: sound and complete. The ideas must make technical sense, even if they don't seem likely to be accepted.
-   The title should accurately describe the content.
-   Edit the MIP for language (spelling, grammar, sentence structure, etc.), markup (Github flavored Markdown), code style

If the MIP isn't ready, the editor will send it back to the author for revision, with specific instructions.

Once the MIP is ready for the repository, the MIP editor will:

-   Assign an MIP number (generally the PR number or, if preferred by the author, the Issue # if there was discussion in the Issues section of this repository about this MIP)

<!-- -->

-   Accept the corresponding pull request

<!-- -->

-   List the MIP in [README.md]

<!-- -->

-   Send a message back to the MIP author with next step.

Many MIPs are written and maintained by developers with write access to the Metaverse codebase. The MIP editors monitor MIP changes, and correct any structure, grammar, spelling, or markup mistakes we see.

The editors don't pass judgment on MIPs. We merely do the administrative & editorial part.

History
-------

This document was derived heavily from [Bitcoin's BIP-0001] written by Amir Taaki which in turn was derived from [Python's PEP-0001]. In many places text was simply copied and modified. Although the PEP-0001 text was written by Barry Warsaw, Jeremy Hylton, and David Goodger, they are not responsible for its use in the Metaverse Improvement Process, and should not be bothered with technical questions specific to Metaverse or the MIP. Please direct all comments to the MIP editors.

  [Bitcoin's BIP-0001]: https://github.com/bitcoin/bips
  [Python's PEP-0001]: https://www.python.org/dev/peps/
  [Metaverse's EIP-0001]: https://github.com/ethereum/EIPs
