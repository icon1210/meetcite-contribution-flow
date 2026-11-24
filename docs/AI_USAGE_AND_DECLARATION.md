# AI Usage and Declaration

This page explains how generative AI has been used in the development of MeetCite. It distinguishes between AI used to help build the software and the AI services that form part of the finished product. The product's speech recognition, meeting-minute generation and evidence-checking pipeline are described in [ARCHITECTURE.md](ARCHITECTURE.md).

The aim is to give a clear account of the tools used, the decisions made by the project team and the checks carried out during development. It is intended for the MSc Information Technology Group 8 project at the University of the West of Scotland, and for anyone reviewing the repository.

Last reviewed: 16 November 2026.

## 1. Overview

Claude Code, Anthropic's AI coding assistant, was used extensively during the development of MeetCite. It supported the team with producing and refining source code, tests, configuration and project documentation. Its use was directed by the project requirements and by instructions and decisions from Olayinka Williams Ajibola ([@icon1210](https://github.com/icon1210)).

AI assistance formed a substantial part of the initial implementation. The tool supported development work, but it was not a member of the project team and did not take responsibility for the project. The people involved in Group 8 set the project aims, agreed responsibilities, considered features, assessed the application, tested its behaviour and made decisions about changes and deployment.

The team is continuing to develop, review and maintain the application. The responsibilities listed below describe how work is allocated; they should not be read as proof that every member has already completed or merged code in their area.

## 2. The project team

MeetCite is the Group 8 MSc Information Technology project for 2026–27. The five team members and their agreed areas of responsibility are:

| Team member | Project role | Main area of responsibility |
|---|---|---|
| Olayinka Williams Ajibola | Project Design Lead | Product direction, system architecture, AI pipeline, interface and UI/UX |
| Oguanya Kenneth Ifeanyi | Group Lead | Database, accounts, migrations and data protection |
| Iloanugo Onyeka Pascal | AI Evaluation Lead | Transcription, speaker identification and C1/C2 evaluation |
| Emmanuel Chieji | Testing, Security and Deployment Lead | Media processing, testing, security and deployment |
| Chinonye Linda Nwanya | Exports and Usability Lead | Exports, follow-up tools, usability and user-study work |

These responsibilities reflect the team's agreed structure. Contributions that have been completed and can be checked in the repository are recorded separately in [CONTRIBUTORS.md](../CONTRIBUTORS.md) and [TEAM_CONTRIBUTIONS.md](TEAM_CONTRIBUTIONS.md). Project work can also include research, planning, report writing, meetings and testing that may not appear as Git commits.

## 3. How AI was used

Claude Code was used as a development assistant across several parts of the project. It helped organise requirements into implementation tasks, suggest technical approaches, generate and refine code and tests, investigate errors and prepare documentation.

| Area | How AI assistance was used | Human direction and responsibility |
|---|---|---|
| Requirements and features | Helped organise requirements and translate them into development tasks | The project team established the project aims and discussed the features needed. Olayinka directed many of the product priorities and requested changes to the application. |
| Technology and architecture | Suggested and helped implement parts of the FastAPI, React, database, transcription and AI stack | Technology choices were considered and accepted or changed by the project team, with Olayinka leading the system design and implementation direction. |
| Backend, frontend and AI pipeline | Helped generate and refine application code, including pipeline, interface, database and deployment work | Olayinka provided implementation instructions, assessed application behaviour and requested revisions. Team members are responsible for understanding and maintaining their assigned areas as development continues. |
| Interface and user experience | Helped build pages, styles, layouts and interactions | Olayinka provided direction on the visual design, content, mascot, mobile layout and user experience. |
| Testing and debugging | Helped create automated tests, interpret failures and propose fixes | The application was also exercised manually. Issues such as slow processing, login problems, colour contrast and mobile layout were reported and prioritised for correction. |
| Deployment | Helped prepare Docker and Caddy configuration, backup scripts and server setup | Olayinka arranged the domain and VPS, configured access and service credentials, and made the decision to deploy the application. |
| Documentation | Helped draft and organise technical and project documentation | The project team is responsible for reviewing the documents and ensuring that submitted academic work accurately reflects the group's work. |

AI suggestions were treated as assistance rather than decisions in their own right. Project direction, feature priorities and deployment decisions remained with the people working on the project.

## 4. Evidence of AI assistance

The repository contains evidence of AI assistance in its commit history and project documentation.

| Evidence | What it records |
|---|---|
| Commit trailers | Seven of the twelve commits on the reviewed version of `main` include a `Co-Authored-By: Claude Opus 5.5` trailer. |
| Other early commits | Five further commits were also prepared with Claude Code, although they do not include a co-author trailer. |
| Development session record | A timestamped record of instructions and changes from 8 October to 13 November 2026 is retained privately by the repository owner. It contains personal and group information and can be made available to the supervisor if requested. |
| Initial repository commit | The first commit, `cc4aaca`, added 175 files and 26,539 lines on 13 October 2026. The initial implementation had been prepared before the repository was created. |
| Project documentation | The [README](../README.md) and [development log](DEVELOPMENT_LOG.md) also describe the use of AI during development. |

The commit history is not a complete record of every interaction with an AI tool. The written declaration therefore explains the wider development process rather than relying on Git attribution alone.

## 5. Review and testing

AI-generated suggestions and code can contain errors, so the application has been checked through automated tests and practical use.

The project's automated checks include:

- Python linting and formatting with Ruff.
- Python type checking with mypy.
- Backend tests with pytest.
- Frontend tests with Vitest and React Testing Library.
- TypeScript checks, frontend linting and production builds.
- Browser-based end-to-end tests with Playwright.

The Playwright suite includes checks of the application at different screen widths, from 320 to 1920 pixels. GitHub Actions is configured to run the relevant checks when changes are pushed.

The owner has also tested application workflows manually, including uploads, longer recordings, live captions and the mobile interface. Feedback from these checks has been used to guide further changes.

These checks provide useful evidence that the application behaves as expected in the tested situations. They do not guarantee that every AI-assisted section is free from defects. At the time of this review, a full line-by-line review of all AI-assisted code by every team member had not yet been completed. That remains part of the team's ongoing review and maintenance work.

## 6. Examples of changes made after review

The application has been revised in response to testing and product feedback. Examples include:

- Adjusting the landing-page colour scheme.
- Simplifying the upload page by removing the privacy box and model choice.
- Correcting dashboard layout overflow found during mobile screen-size testing.
- Revising the user-study design so that participants are not recorded.

These examples show how development output was assessed against the project's requirements and changed when it did not meet them.

## 7. Ongoing team review and responsible use

As the project moves forward, the team will continue to use a review process for new work:

- Members should work through their own GitHub accounts and branches, following the process in [CONTRIBUTING.md](../CONTRIBUTING.md).
- Pull requests should state whether AI tools were used and describe the assistance provided.
- Changes should be reviewed and tested before they are merged.
- Each member should become familiar with the implementation in their area and be able to explain the relevant design choices and limitations.
- Completed work should be recorded in [TEAM_CONTRIBUTIONS.md](TEAM_CONTRIBUTIONS.md), with links to repository evidence where available.

The contribution records distinguish assigned responsibilities from work that has already been completed and verified. This helps the team recognise everyone's role without overstating what the commit history currently demonstrates.

## 8. Declaration

Group 8 acknowledges that generative AI, including Claude Code, was used extensively as a development aid during the creation of MeetCite. AI assistance contributed to the preparation and refinement of code, tests, configuration and documentation.

The project was directed and developed under the responsibility of the human project team. The team remains accountable for the requirements, design decisions, review, testing, maintenance and final submission, and will disclose the use of AI in accordance with the University's academic requirements.

AI tools are not members of Group 8 and are not presented as human contributors. This declaration records their role as development tools while recognising the responsibilities of the students who developed and continue to maintain the project.
