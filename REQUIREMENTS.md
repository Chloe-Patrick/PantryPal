# PantryPal — Requirements Backlog

## Project Overview

PantryPal is a cooking application designed to help users find recipes using ingredients they already have available. Users can enter their ingredients, receive matching recipe suggestions, and filter recipes based on their preferences. The application aims to make meal planning easier, reduce food waste, and make cooking more accessible to beginners.

**Development Methodology:** Kanban

**Requirements Elicitation Method:** Initial requirements generated using ChatGPT and organized into user stories with priorities, acceptance criteria, and dependencies.

## Product Backlog

| ID | Requirement / User Story | Priority | Dependencies |
|---|---|---|---|
| R01 | As a user, I want to enter ingredients I have available so that I can find recipes using those ingredients. | High | None |
| R02 | As a user, I want to edit or remove ingredients from my list so that I can keep my available ingredients accurate. | High | R01 |
| R03 | As a user, I want to receive recipe suggestions based on my available ingredients so that I can decide what to cook. | High | R01 |
| R04 | As a user, I want to view recipe instructions so that I can follow the steps to prepare a meal. | High | R03 |
| R05 | As a user, I want to see which ingredients I am missing from a recipe so that I know what I need to purchase. | High | R01, R03 |
| R06 | As a user, I want to filter recipes by dietary restrictions so that I can find meals suitable for my needs. | Medium | R03 |
| R07 | As a user, I want to filter recipes by cooking time so that I can find meals that fit my schedule. | Medium | R03 |
| R08 | As a user, I want to search for recipes by name or category so that I can explore meals without entering ingredients. | Medium | Recipe database |
| R09 | As a user, I want to save my favorite recipes so that I can easily find them again. | Medium | R03, R04 |
| R10 | As a user, I want to create an account so that I can save my ingredients and preferences between sessions. | Medium | None |
| R11 | As a user, I want to create a grocery list of missing ingredients so that I can shop more efficiently. | Medium | R05 |
| R12 | As a user, I want to view recipes on my phone or computer so that I can use the application wherever I cook. | High | None |
| R13 | As a user, I want a simple, accessible interface so that I can navigate the application regardless of my cooking or technical experience. | High | None |
| R14 | As a user, I want to see recipe preparation time and difficulty so that I can choose recipes appropriate for my skill level. | Medium | R03 |
| R15 | As a user, I want to receive alternative ingredient suggestions so that I can still prepare meals when I am missing an ingredient. | Low | R05 |

## Acceptance Criteria

| ID | Acceptance Criteria |
|---|---|
| R01 | Users can add one or more ingredients to a list. |
| R02 | Users can update or delete previously entered ingredients. |
| R03 | The system displays recipes ranked by how many required ingredients the user has available. |
| R04 | Each recipe displays an ingredient list and step-by-step cooking instructions. |
| R05 | The system clearly identifies which required ingredients are missing. |
| R06 | Users can select dietary restrictions and filter results accordingly. |
| R07 | Users can set a maximum cooking time and see recipes meeting that limit. |
| R08 | Users can search recipes by keyword or category. |
| R09 | Users can save recipes and access their saved recipes later. |
| R10 | Users can register, log in, and retrieve their saved data. |
| R11 | Users can add missing ingredients from a recipe to a grocery list. |
| R12 | The interface adapts to desktop and mobile screen sizes. |
| R13 | Users can navigate core features using a keyboard, and interface controls have descriptive labels. |
| R14 | Recipe results display estimated preparation time and difficulty level. |
| R15 | The application displays possible ingredient substitutions when substitution data is available. |

## Nonfunctional Requirements

| ID | Requirement | Priority |
|---|---|---|
| NF01 | Recipe searches should return results within 3 seconds under normal operating conditions. | Medium |
| NF02 | The application should use responsive design to support mobile devices and desktop computers. | High |
| NF03 | User passwords and personal information must be stored securely using appropriate security practices. | High |
| NF04 | The interface should follow WCAG 2.2 Level AA accessibility guidelines for applicable features. | High |
| NF05 | The application should display helpful messages when no matching recipes are found or a request fails. | Medium |

## Dependency Overview

The initial development will focus on the core recipe recommendation functionality.

- **R01 → R03 → R04:** Users must enter ingredients before the application can recommend matching recipes, and recipe results must be available before users can view recipe details.
- **R01 + R03 → R05 → R11:** Missing ingredients must be identified before users can generate grocery lists.
- **R03 → R06, R07, R14:** Dietary filtering, cooking-time filtering, and recipe metadata build on the basic recommendation system.
- **R05 → R15:** Ingredient substitutions depend on knowing which ingredients are missing.
- **R10 → Persistent saved data:** User accounts support storing ingredients, preferences, and saved recipes between sessions.

## Minimum Viable Product (MVP)

The first version of PantryPal will focus on the application's most important features:

1. Entering, editing, and removing ingredients (R01–R02).
2. Receiving recipe recommendations based on those ingredients (R03).
3. Viewing recipe instructions (R04).
4. Identifying missing ingredients (R05).
5. Providing a responsive and accessible user interface (R12–R13).

Additional features such as dietary filters, user accounts, grocery lists, and ingredient substitutions can be introduced in later development stages.

## Kanban Workflow

The project will use a Kanban board with five columns:

**Backlog → To Do → In Progress → Testing → Done**

Requirements will be selected based on priority and dependencies rather than assigned to fixed Scrum sprints. This allows development to remain flexible while tracking progress and completing higher-priority features first.

## Assumptions and Open Questions

This is an initial requirements backlog. The following details will need clarification during further requirements elicitation:

- Will recipes come from an external API or an application-managed database?
- Will users be able to access recipe recommendations without creating accounts?
- Will the application support ingredient quantities or only ingredient names?
- Will missing ingredients be allowed in recommended recipes, and how many?
- Will users be able to submit their own recipes?

These questions will be reviewed as the project requirements become more detailed.
