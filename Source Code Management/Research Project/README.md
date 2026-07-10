# Source code Management Research project
Source code management systems are powerful tool designed to manage changes and facilitates collaborative development throughout the software development lifecycle. SCM has two major category which are centralized version control system(CVCS) and distributed version control system(DVCS) respectfully.
Git enhances modern software development by enabling efficient collaboration, accurate tracking of changes, and flexible branching for organized workflows. It improves development speed through fast local operations and ensures data safety by maintaining complete copies of the repository across all users.

## Historical context
Before Git, Developers use manual approach(copying files) and later centralized version control systems such as CVS and Subversion was introduced to enhance the software development process. This system introduced a central repository where all codes are stored. Limitation of previous version control systems includes slow performancre, dependence on the central repository, difficulty branching and merging, and no working offline.

### Key features of Git
Git was developed to solve CVCS limitation by introducing new efficient features which are as follow:
- Offline capabilities: Distributed version control system allow developers to copy the entire project history and work on new features offline
- parallel development: developers are allowed to create new branches, work on different features, and bug fixes simultaneously
- Data redundancy: Git ensure data integrity storing data using hashing. It know about every changes which makes it easy to revert to previous changes and retrieve deleted or lost data.

### Advantages of Git
Git improves source code management by enabling effective collaboration through branching, allowing multiple developers to work simultaneously. It provides accurate version tracking by recording all changes and maintaining project history. Additionally, it integrates seamlessly with CI/CD tools to automate building, testing, and deployment, resulting in faster and more reliable software development.

### Challenges and solution
Git presents challenges such as a difficult learning curve, merge conflicts, complex workflows in large teams, and inefficiency with large files. These issues can be mitigated through proper training, use of standard workflows (e.g., Git Flow), clear commit practices, regular updates to reduce conflicts, and tools like GitHub Desktop or Git LFS to simplify usage and improve performance.

Git is a distributed version control system, unlike SVN and Perforce which are centralized. This allows Git to offer faster performance through local operations, offline work, and more flexible collaboration. Mercurial is similar to Git but has lower adoption.

### Case study and industry adoption
Organization uses Git for structured workflow, branching, pull requests, and CI/CD integration to manage code efficiently. Key aspect include the need for clear workflows, proper training, consistent commit practices, automation, and strong code review and access control to ensure successful Git adoption.

### Security best practice
Secure Git access is achieved by applying least-privilege permissions through role based access control (RBAC) and enforcing MFA for all users. Additionally, using secure authentication methods like SSH keys or HTTPS with tokens helps protect repositories from unauthorized access.

Secure cloud-based repositories by enforcing strong access controls (RBAC), enabling MFA, avoiding hardcoded secrets, and regularly auditing permissions and activity. Use encryption to protect data at rest and in transit, and adopt secure protocols like SSH keys or HTTPS with tokens to ensure only authorized users can access repositories and data.

Ensure effective logging and auditing by enabling detailed activity logs for all repository actions (commits, merges, pushes) and regularly reviewing them. Implement audit trails, restrict log access, and integrate monitoring tools to track changes. Use automated alerts to notify teams of unusual activities, such as unauthorized access, force pushes, or changes to critical branches, allowing quick response to potential security threats.

### Future trends
Emerging trends in source code management include increased automation, cloud-based development, AI-assisted coding, and deeper DevOps integration. Git is evolving by improving performance, security features, and seamless integration with CI/CD tools.

Advancements in DevOps and CI/CD are making Git central to automated workflows, enabling continuous integration, testing, and deployment. This leads to faster development cycles, improved collaboration, and more efficient software delivery.

