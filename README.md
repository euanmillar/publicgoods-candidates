# Nominees, Candidates and Digital Public Goods

Welcome! 👋 We are glad that have found this repo and you are interested in Digital Public Goods, and using technology to make this world  a more just and equitable one. We are in this together: the more the greater impact!

This repository is used to manage the process of adding nominees for consideration as [Digital Global Public Goods](https://digitalpublicgoods.net/public-goods/). This is one of four interconnected repositories; refer to the [publicgoods-website](https://github.com/unicef/publicgoods-website) for an overview.

## How to nominate a Digital Public Good

1. Go to the [nominees](https://github.com/unicef/publicgoods-candidates/tree/master/nominees) folder, and click on `Create new file`
2. Name the new file with the name of the digital public good in [kebab-case](https://wiki.c2.com/?KebabCase), and `.json` as the extension. For example: [wikipedia.json](https://github.com/unicef/publicgoods-candidates/blob/master/nominees/wikipedia.json) or [inlcusion-ukr.json](https://github.com/unicef/publicgoods-candidates/blob/master/nominees/inclusion-ukr.json)
3. Use the [template](https://github.com/unicef/publicgoods-candidates#template) from the section below to include the requested information. Be sure to include the fields marked `REQUIRED` with the corresponding information, as well as any `OPTIONAL` fields. Delete any lines marked `OPTIONAL` that you don't want to include. For the `license` field, be sure to use an approved [SPDX identifier](https://spdx.github.io/spdx-spec/appendix-I-SPDX-license-list/#i1-licenses-with-short-identifiers).
4. Scroll down and accept the suggested field for the commit message `Create <filename>`, and choose `Create a new branch for this commit and start a pull request`. Click on `Propose new file`
5. You are taken to a new page where you can leave a comment about the file you are about to propose to add, and finally click on `Create Pull Request`
6. Wait for the green checkmark to say `All checks have passed` to have confirmation that the file complies with the expected format, and is ready to merge pending a review.

## Template

```
{
        "name": "REQUIRED",
        "aliases": "[OPTIONAL: Array of strings - Abbreviations, initialisms, or alternate names, where relevant",
        "description": "REQUIRED",
        "license": [REQUIRED, Array of objects:
                {
                        "spdx": "SDPX identifier for this license",
                        "licenseURL": "Link to the license under which this nominee is released"
                }
        ],
        "website": "REQUIRED",
        "SDGs": [REQUIRED, Array of objects listing SDGs by number and name],
        "type": [REQUIRED, Array of strings, multiple choice from "software", "data", "standards"],
        "repositoryURL": "OPTIONAL: Link to main repository",
        "sectors:" [OPTIONAL: Array of strings - List of sectors that this nominee addresses.]
        "organizations": [REQUIRED, Array of objects: 
                {
                        "name": "REQUIRED - Name of the organization",
                        "website": "OPTIONAL - Website of the organization",
                        "contact_name": "OPTIONAL - Name of contact individual in the organization",
                        "contact_email": "OPTIONAL - Email for contact individual in the organization",
                        "org_type": "REQUIRED - One of 'owner, 'maintainer', 'funder' or 'implementer'
                }
        ]
}
```

## Requirements and Considerations

For those projects that match [the initial set of requirements](https://digitalpublicgoods.net/nominate/), anyone can open a [Pull Request](https://github.com/unicef/publicgoods-candidates/pulls) on this repository as a submission following these guidelines:
- Data for each nominee is stored as a JSON file. JSON ([JavaScript Object Notation](https://www.json.org)) is a lightweight data-interchange format. It is easy for humans to read and write. It is easy for machines to parse and generate.
- Each nominee json file is kept under the `nominees/` folder, add yours there. Use any other of the existing nominees as a reference for what fields to include, and how to enter the required information.
- Each nominee json file is validated using the [JSON-schema](https://json-schema.org) found at the root of this repository: [nominee-schema.json](nominee-schema.json). Each submission needs to pass the automated validation (`continuous-integration/travis-ci`) before being merged into the existing repository.
- The `license` field is standardized using [SPDX identifiers](https://spdx.github.io/spdx-spec/appendix-I-SPDX-license-list/#i1-licenses-with-short-identifiers).

From the set of nominee json files, [this list](https://digitalpublicgoods.net/explore/) of Digital Global Public Goods is automatically generated and kept in sync with the contents of this repo.

## License

```
This is free and unencumbered software released into the public domain.

Anyone is free to copy, modify, publish, use, compile, sell, or
distribute this software, either in source code form or as a compiled
binary, for any purpose, commercial or non-commercial, and by any
means.
```

All the information compiled and aggregated in this repository is already in the public domain, thus  we dedicate this software to the public domain. As a result, we impose no limitations nor requirements of any kind of how you use it or reuse it. As a courtesy on your part, we would very much appreciate hearing from you either on how you are using the information in this repo, or any great ideas on how we can collaborate together.
Email us at hello@digitalpublicgoods.net 💌