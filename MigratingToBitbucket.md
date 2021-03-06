[Bitbucket](https://bitbucket.org) has been providing both public private source hosting to the internet since 2008. This document will cover how to migrate a project on Google Code to Bitbucket. However, Bitbucket only supports the Mercurial and Git protocols. SVN-based projects can be imported, but will be converted as part of the migration.

# Sign in to Bitbucket #
If you do not already have a Bitbucket account, create one and log in. You do not need to create a new Bitbucket project before importing your Google Code project; when you start the importer tool, the Bitbucket project will be created for you.

# Create a new Project via Import #
Once you have logged into Bitbucket, simply click Create to begin creating a new repository and then click the "importing a repository" link.

That will lead you to a simple wizard for importing projects. Select "Google Code" from the Source combo box, and then enter your Google Code project name. You can find more information in the [Bitbucket Import documentation](https://confluence.atlassian.com/display/BITBUCKET/Import+code+from+an+existing+project).

The Bitbucket importer may take a few minutes to import your project, depending on the size of your repo.

Note that the "Issue tracking" and "Wiki" checkboxes are for whether or not you want your Bitbucket project to have the Issue tracking and Wiki _features_. Bitbucket will not import your Google Code issues or wikis. You will need to run separate tools to export that data from Google Code.

# Project Issues #
To export project issues to Bitbucket, see the documentation for the [Issue Exporter](IssueExporterTool.md).

# Project Wikis #
To export project wikis to Bitbucket, see the documentation for the [Wiki-to-Markdown Tool](WikiToMarkdownTool.md).

# URL Redirection #
Once a project has been successfully exported to Bitbucket, you will want to update your project's homepage on Google Code to avoid confusion.

Some project owners simply update their project homepage's text to indicate it has moved. For example [subtext](http://code.google.com/p/subtext) or [bwapi](http://code.google.com/p/bwapi).

Another option is to set the Google Code "project moved" flag. When set, attempts to access the project will take users to an interstitial page indicating the new project location. In the future, the page will automatically redirect your new project on bitbucket.org.

To set the "project moved" flag, navigate to your project's advanced admin page, at https://code.google.com/p/project-name/adminAdvanced.

Once there, enter the new project home page URL under "project moved". For example: https://bitbucket.org/larryp/search_engine. Finally click the "Project Moved" button.