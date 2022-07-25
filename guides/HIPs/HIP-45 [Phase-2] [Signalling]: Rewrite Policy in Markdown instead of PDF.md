# HIP-45 [Phase-2] [Signalling]: Rewrite Policy in Markdown instead of PDF
```
HIP: 45
title: Rewrite Policy in Markdown instead of PDF
author: @greenlucid
status: Phase 2
created: 2022-06-23
conflicts with: None
languages: EN
```

## Simple Summary

Migrate the policy from PDF to Markdown, and edit the policy in a repository.

## Abstract

Policies should be written and edited in Markdown. This makes coordination easier and, in particular, speeds up policy editions, even more so when dealing with concurrent HIPs. A repository will be built under [Proof of Humanity GitHub](https://github.com/Proof-Of-Humanity/) for this purpose. 

## Motivation

Using pdf as the raw document for a policy is a coordination disaster. There is too much friction around making changes to the policy to integrate the HIPs that affect it. With a PDF, the latest working document must also be made available, which introduces delays. Also, to make this new quality of life explicit, a repository will be used to coordinate the changes. 

## Rationale

The format should be easy to edit, audit, and replicate. The format should make it easy to follow changes and notice mistakes, just like code repositories do. Code repositories are the state of the art solution to coordinate changes across technical files (*source code*), so it makes sense to also use a repository for a critical document such as the PoH registration policy.

The official [Proof of Humanity GitHub](https://github.com/Proof-Of-Humanity/) was chosen as a default option, but this HIP does not mandate it must be the only repository to use. Although, it is recommended to contribute all changes in the same repository, for clarity.

## Implementation

Make a repository for the express purpose of containing this policy, or other important files (such as the `MetaEvidence` jsons). This rewrite of the policy will be the starting basis for the repository:

[poh-policy.md](https://github.com/greenlucid/poh-policy/blob/master/poh-policy.md) (feel free to make PRs to fix issues during this Phase 2)
[Rendered sample](https://ipfs.kleros.io/ipfs/QmTbxCZQL28w6TFgJ6XBPqmBuw2eeNtR9T5u3tYJgEJhLt/Proof%20of%20Humanity%20Registry%20Policy.pdf) (this render is not particularly good)

The process to edit and champion HIPs that modify the policy should be the following:

* The champion of the HIP forks the repository containing the policy.
* The champion creates a draft Pull Request to the base repository with the name of the HIP and a link to the HIP in the description.
* The champion writes the changes to the policy, and asks for reviews and feedback. This can be done during Phase 1 or Phase 2.
* After the feedback process, the PR stops being a Draft and no further changes are allowed. The HIP then gets to Phase 3.
* If the HIP passes, the PR is merged.

---

## Addendum - FAQ

### Who are “the reviewers”?

This is purposely under-specified. It could just be voluntaries or enthusiasts, but there’s no explicit need for them to be authority figures, or Mission Board members. My suggestion is that a few eyes that don’t agree with the HIP should also take a look.

### Isn’t this complicated for non-technical contributors?

It’s certainly not harder than what we currently have. But, if this was the case, I will write a short guide on how to join a repository and follow the steps for non-technical people to champion or contribute to HIPs.

### Won’t it be ugly for the users to show a raw text file?

This HIP does not set into stone that the raw markdown file must be the policy provided in the `MetaEvidence`. But, it is possible to use a browser extension to render markdown dynamically. [This is such an example](https://github.com/KeithLRobertson/markdown-viewer).

It is also possible to use an app such as [md2pdf](https://md2pdf.netlify.app/) to render the markdown as a pdf file, and then include that file in the `MetaEvidence`. But this creates an extra step that should be scrutinized.

### Where is the markdown policy kept?

It doesn’t matter if it’s published as a raw markdown or published as pdf, it should be kept in a repository in any case, to allow following the process indicated in the *implementation* header.
As for the specific question of, in which repository, I would suggest to use the [official Proof of Humanity GitHub repository ](https://github.com/Proof-Of-Humanity/).
