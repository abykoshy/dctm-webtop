# Packaging Documentum client war like Webtop with custom configuration and code
There are many ways of packaging Webtop/WDK Customizations into your application. The most simple would be to include the out-of-the-box Webtop/WDK war contents into your project and then package it like a regular war. The disadvantages in this approach are

- Creation of branches/tags in the version control system will consume a lot of space as the Webtop/WDK war is ~200 MB and a constant cleanup would be required.

- Upgrades/Patches are normally managed by the administration team and a manual update in the version control has to be made in order to apply these patches on the project.

Decoupling the out-of-the-box Webtop/WDK from your project would be the solution to rectify these. And this can be achieved by using the Maven Overlay feature. With this, a particular war can be superimposed(overlayed) with the customizations.
