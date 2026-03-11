# Foundations of Project Management

### Introduction: What is Project Management?

Project Management is the discipline of planning, organizing, motivating, and controlling resources to achieve specific goals. Every project is a temporary endeavor; it has a defined beginning and end, and a specific scope and budget. The ultimate goal is to deliver value to the organization or customer.

---

# Part 1: The Evolution of Frameworks (The Methodologies)


## Chapter 1: The Traditional Approach – Waterfall

Before software, there was manufacturing and construction. This is where the Waterfall methodology originated. It’s a linear, sequential approach where each phase must be completed before the next one begins.

### The Workflow:

1. **Requirements Gathering**: Define exactly what is being built, in exhaustive detail.
2. **System Design**: Architects design the technical solution based on the requirements.
3. **Implementation (Coding)**: Developers build the product.
4. **Testing (QA)**: The complete product is tested for bugs against the initial requirements.
5. **Deployment**: The product is delivered to the customer.
6. **Maintenance**: Fixing issues post-launch.

### Benefits:

Predictability: Clear timelines and budgets if requirements don’t change.
Discipline: Structured documentation and approval gates.
Simplicity: Easy to understand and manage for straightforward projects.

### The Downfall in Software: 
Waterfall assumes requirements are fixed. In software, requirements always change. This led to massive project failures: projects delivered over budget, behind schedule, and with features the customer no longer needed.


<img width="459" height="741" alt="Screenshot 2026-03-10 at 7 49 42 PM" src="https://github.com/user-attachments/assets/b9232951-b6c3-4ddc-9306-287857a8c4d8" />


## Chapter 2: The Modern Approach – Agile

Agile isn't a single methodology; it's a philosophy formalized in the Agile Manifesto (2001). It was created by software developers frustrated with Waterfall. It prioritizes:

- **Individuals and interactions** over processes and tools.
- **Working software** over comprehensive documentation.
- **Customer collaboration** over contract negotiation.
- **Responding to change** over following a plan.

### Key Concepts: 
**Iterative** (doing things repeatedly) and **Incremental** (adding small pieces). Instead of one big release, you release small, working parts of the software frequently.

<img width="455" height="735" alt="Screenshot 2026-03-10 at 7 35 42 PM" src="https://github.com/user-attachments/assets/086cc171-6878-478b-beeb-ffe04ac1f8fa" />


## Chapter 3: Implementing Agile – Scrum & Kanban

Agile is the philosophy; Scrum and Kanban are the frameworks used to do Agile.

### Scrum: A highly structured Agile framework.

- **The Sprint**: A fixed period (usually 2-4 weeks) where a specific set of work must be completed.
- **Roles**: Product Owner (represents the customer), Scrum Master (facilitator/coach), Development Team.
- **Ceremonies**: Sprint Planning, Daily Stand-up (15 mins), Sprint Review (demo), Sprint Retrospective (team reflection).

### Kanban: A flexible framework focused on continuous delivery and managing flow.

- **The Kanban Board**: Visualizes work using columns (To Do, In Progress, Done).
- **WIP Limits**: Restricting the amount of work in progress to prevent bottlenecks.
- **Flow**: Work moves through the board continuously, rather than in fixed sprints.

<img width="462" height="735" alt="Screenshot 2026-03-10 at 7 40 09 PM" src="https://github.com/user-attachments/assets/ca896ac1-f9ee-4114-a069-7852cbe485b7" />


## Chapter 4: The Best of Both Worlds – Hybrid

Many companies use a Hybrid approach. They might use Waterfall for high-level planning and budgeting but switch to Agile (Scrum or Kanban) for the day-to-day development work.

---

# Part 2: Project Management in SaaS Companies

Software as a Service (SaaS) companies develop and maintain software hosted in the cloud. They are almost universally Agile because they need to deploy updates frequently (sometimes daily) based on user feedback.

## Chapter 5: Tools of the Trade

To manage Agile at scale, SaaS companies rely heavily on specialized tools.

### Jira: The Agile Workhorse
Jira (by Atlassian) is the industry standard for software project management. It tracks tasks, bugs, and agile progress.

- **Issues**: Everything in Jira is an "Issue" (a story, bug, or task).
- **Epics**: Large bodies of work that can be broken down into smaller issues.
- **Boards**: Scrum and Kanban boards are central to Jira, visualizing the flow of tasks.
- **Workflows**: Customizable pathways an issue follows (e.g., Backlog → In Progress → Dev Complete → QA → Done).

### GitHub/GitLab: Where Code Lives
These are version control platforms. Developers write code, and these tools manage the history of changes. This is crucial when multiple developers work on the same project simultaneously.

### Why Connect Jira and GitHub? (The Essential Link)
Jira manages the management task (e.g., "Fix login bug"). GitHub manages the technical task (the actual code changes).

- **The Connection**: Developers create a unique branch in GitHub for their Jira issue (e.g., `feature/JIRA-123-fix-login`).
- **The "Why"**: Linking them automates visibility.
- When a developer commits code or opens a "Pull Request" (asking to merge code) in GitHub, Jira automatically updates the status of the corresponding issue (e.g., moves it from "In Progress" to "Code Review").
- This allows PMs to see the real-time status of the code without asking developers.

### Zendesk: The Voice of the Customer
Zendesk is a customer service platform. It's where customers submit support requests (tickets).

#### The Jira-Zendesk Link (Support to Development)

1. A customer submits a ticket in Zendesk about a bug.
2. The support agent confirms it's a bug.
3. Instead of re-typing everything, the agent uses an integration to create a linked Jira issue directly from the Zendesk ticket.
4. When developers fix the bug and close the Jira issue, the Zendesk ticket can be automatically updated or solved, and the support agent can notify the customer.

<img width="457" height="738" alt="Screenshot 2026-03-10 at 7 37 17 PM" src="https://github.com/user-attachments/assets/daace50b-b127-432a-8d75-00a5dc044254" />


## Chapter 6: Product Ideation and Roadmapping

How do SaaS companies decide what to build next?

1. **Ideation**: Collecting ideas from customers (via Zendesk/feedback portals), sales teams, competitors, and internal brainstorms.
2. **Prioritization**: PMs evaluate ideas based on business value, effort, and strategic alignment (often using frameworks like RICE: Reach, Impact, Confidence, Effort).
3. **Product Roadmap**: A high-level, visual summary showing the vision and direction of the product offering over time. This roadmap is then broken down into Epics and User Stories in Jira for the development team.

---

## Chapter 7: Version Control and Releases

How is software deployed to users?

### Version Control (Git):
- **Branching**: Developers create isolated "branches" of the main codebase to work on new features or bugs.
- **Merging**: When done, the branch is merged back into the main codebase after passing review and testing.

### Releases (Semantic Versioning - SemVer):
Releases are packaged versions of the software. SemVer uses three numbers: `Major.Minor.Patch` (e.g., 2.3.1).

- **Patch (1)**: Backward-compatible bug fixes.
- **Minor (3)**: Backward-compatible new features.
- **Major (2)**: Major changes that may break existing functionality (breaking changes).

### Release Management: 
The process of moving a version through stages (Development → Testing/Staging → Production/Live) and managing the actual deployment, including rollback plans if things go wrong.

<img width="2816" height="1536" alt="ProjectManagement" src="https://github.com/user-attachments/assets/3b4f01a4-3be0-4923-b9ab-d30a557a0aab" />
