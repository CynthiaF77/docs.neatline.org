---
layout: default
---
# Managing User Permissions

## At a glance

  - Neatline has a simple user permissions system integrated into Omeka, designed to make it easy to use Neatline with groups of all sizes.
  - **Researcher** users can view public Neatline exhibits, but don't have access to any of the administrative features.
  - **Contributor** users can create and modify their own Neatline exhibits, but can't make changes to other users' exhibits.
  - **Admin** and **Super** users can do everything: create, modify, and delete Neatline exhibits created by all users.
  - When [groups of users](user-permissions.html#working-with-user-groups) need to work together as a team on a single exhibit, or a set of exhibits, assign one **Contributor** account to be used by the whole group.

## User Levels and Access

Neatline uses the built-in ACL (Access Control List) system in Omeka, which defines a series of user "roles" for site administrators, each with a different level of access. You can find the list of users and add new ones by clicking the "Users" tab on the top navigation bar when logged into your Omeka site (see the [Omeka documentation][omeka-acl] for more information about how to create and manage user roles). 

Defining user permissions allows you to control access to Neatline exhibits when working with multiple users, and can help in avoiding issues like one user modifying or deleting a Neatline exhibit created by another user. If you are working with a small group of trusted collaborators, you may want to allow everyone to have access to all work on the site, no matter the creator. However, if you're using Neatline with large numbers of people - for example, if you're teaching a 200-person lecture course, and want to use Neatline for an assignment - setting user permissions is critical to prevent users from accidentally changing settings or deleting content. 

**Read through the following user roles and their Neatline access to determine what works best for your project:**

- **Researcher** users are completely locked out of Neatline - they can't create, edit, or delete exhibits. Effectively, researchers have the same level of access as an anonymous, public user - they can view published exhibits, but nothing else. This conforms with Omeka's definition of the Researcher role, which was originally added so that site administrators could make it possible for certain users to _view_ non-public items, without being able to modify content on the site.

- **Contributor** users can create, edit, and delete _their own Neatline exhibits_, but can't make changes to anyone else's exhibits. This is the role that's best suited for students, workshop participants, and other users who need to be able to work with their own Neatline content, but who don't need to make high-level changes to the site (eg, changing themes, installing plugins).

- **Admin** and **Super** users can do everything - they can create, modify, and delete Neatline exhibits created by all users. Super and Admin users have different levels of access in Omeka, see the [Omeka documentation][omeka-acl] for more details. 

## Working with User "Groups\"

User roles can only be assigned to individual users - Omeka has no notion of a "group" of users. This is problematic if you want to allow teams of users to work collaboratively on the same exhibit. It doesn't work to create separate **Contributor** accounts for each of the users, which would allow each individual user to create her _own_ exhibits, but not for the entire group to make edits to the same exhibit. You could always just make all of the users **Admin** users, but that may not be ideal for your needs - everyone would be able to edit _everyone_ else's content, not just the exhibits that are "owned" by the group.

For now, the easiest way to allow groups of users to work together on a single exhibit, or a set of exhibits, is to create a single **Contributor** account for each group. So, if you have 10 groups, each comprised of 4 students, create 10 different **Contributor** accounts and give the same set of login credentials to all 4 students in each of the 10 groups. This way, users can edit exhibits and records created by anyone else in their own group, but not exhibits created by anyone in a different group.

**Related:** [Omeka Documentation][omeka-acl], [Managing Exhibits](managing-exhibits.html)

[omeka-acl]: http://omeka.org/codex/Managing_Users_2.0
