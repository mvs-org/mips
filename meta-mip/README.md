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
    -   **Core** - improvements requiring a consensus fork (e.g. [MIP5], [MIP101]), as well as changes that are not necessarily consensus critical but may be relevant to “core dev” discussions (for example, [MIP90], and the miner/node strategy changes 2, 3, and 4 of [MIP86]).
    -   **Networking** - includes improvements around [devp2p] ([MIP8]) and [Light Metaverse Subprotocol], as well as proposed improvements to network protocol specifications of [whisper] and [swarm].
    -   **Interface** - includes improvements around client [API/RPC] specifications and standards, and also certain language-level standards like method names ([MIP59], [MIP6]) and [contract ABIs]. The label “interface” aligns with the [interfaces repo] and discussion should primarily occur in that repository before an MIP is submitted to the MIPs repository.
    -   **ERC** - application-level standards and conventions, including contract standards such as token standards ([ERC20]), name registries ([ERC26], [ERC137]), URI schemes ([ERC67]), library/package formats ([MIP82]), and wallet formats ([MIP75], [MIP85]).

-   An **Informational MIP** describes a Metaverse design issue, or provides general guidelines or information to the Metaverse community, but does not propose a new feature. Informational MIPs do not necessarily represent Metaverse community consensus or a recommendation, so users and implementers are free to ignore Informational MIPs or follow their advice.
-   A **Meta MIP** describes a process surrounding Metaverse or proposes a change to (or an event in) a process. Process MIPs are like Standards Track MIPs but apply to areas other than the Metaverse protocol itself. They may propose an implementation, but not to Metaverse's codebase; they often require community consensus; unlike Informational MIPs, they are more than recommendations, and users are typically not free to ignore them. Examples include procedures, guidelines, changes to the decision-making process, and changes to the tools or environment used in Metaverse development. Any meta-MIP is also considered a Process MIP.

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

Some Informational and Process MIPs may also have a status of “Active” if they are never meant to be completed. 
See details in [MIP 1](./MMIP-1.md).
