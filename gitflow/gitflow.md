Por branching strategy
¿por qué elegir este branching strategy? -- casos de uso
steps per branch - (procesos-> workflow del desarrollo en esa estrategia) How to?(guide)
buenas prácticas para mantener la estrategia de branching limpia (overview particular)

# Why to choose Gitflow?

**Clear Branching Model**: GitFlow defines a set of well-defined branches with specific purposes, such as feature branches for new features, release branches for preparing releases, and hotfix branches for fixing critical issues in production. This clear model makes it easier for team members to understand how code changes flow through the repository.

**Separation of Concerns**: GitFlow separates long-lived branches from short-lived ones. For instance, feature branches contain only changes related to a specific feature and are merged into the develop branch when complete. This segregation helps maintain a cleaner history and simplifies code review and integration.

**Support for Parallel Development**: GitFlow facilitates concurrent development of multiple features by creating separate branches for each feature. This enables teams to work on different features simultaneously without interfering with each other's work.

**Release Management**: The GitFlow workflow includes dedicated release branches where the code is prepared for deployment. This allows for last-minute bug fixes and quality assurance before deploying the code to production.

**Hotfixes**: GitFlow provides a structured way to handle urgent bug fixes in production. Hotfix branches are created from the master branch, allowing for quick fixes without disturbing ongoing development.

**Consistency**: By using GitFlow, teams can establish consistent practices for version control and collaboration. This consistency improves code stability, reduces conflicts, and enhances overall development efficiency.

**Tooling and Community Support**: GitFlow has been around for a while, and as a result, many Git tools and services (e.g., Git clients, continuous integration tools) have built-in support for its workflow. Additionally, there's a vast community that can offer guidance and best practices for implementing GitFlow in different scenarios.

# How to implement succesfully Gitflow?

