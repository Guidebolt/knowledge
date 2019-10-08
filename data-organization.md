# Data Organization

Our data organization policy should be understood from the perspective of each individual member.

Each member manages 3 primary data categories:

* PERSONAL SECRET: This includes sensitive personal data such as password databases and confidential government documents. Dangerous if accessed by unauthorized parties.
* PERSONAL PRIVATE: This includes knowledge that is valuable enough to be recorded and roughly organized. Not overly damaging if leaked.
* COMPANY PUBLIC: This includes information that is sufficiently organized, accurate, recommendable, and valuable for the intended audience. Freely available and backed by the company's reputation.

Data generally exists as files and folders with 3 types of access/preservation:

* SIMPLE: Normal files and folders. No changelog. Deletion is permanent. 
* VERSION-CONTROL: Normal files and folders with a version control system like git. All changes can be reverted.
* DATABASE: Info is stored inside a set of database files. All changes must follow specific database syntax, often edited through a DB client-console or USER application.

