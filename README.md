# Project Template Migration

This solution will add the Action, "GetProjectTemplateAML", to the Project Template ItemType. This action can be used to migrate a Project Template item from one database to another.

## History

Release | Notes
--------|--------
[v3.1](https://github.com/ArasLabs/project-template-migration/releases/tag/v3.1) | Confirmed for 11.0 SP15
[v3.0](https://github.com/ArasLabs/project-template-migration/releases/tag/v3.0) | Confirmed for 11.0 SP7, 11.0 SP5
[v2.1](https://github.com/ArasLabs/project-template-migration/releases/tag/v2.1) | Bug fixes
[v2.0](https://github.com/ArasLabs/project-template-migration/releases/tag/v2.0) | Confirmed for 10.0 SP5
[v1.0](https://github.com/ArasLabs/project-template-migration/releases/tag/v1.0) | Initial Release

#### Supported Aras Versions

Project | Aras
--------|------
[v3.1](https://github.com/ArasLabs/project-template-migration/releases/tag/v3.1) | 11.0 SP15
[v3.0](https://github.com/ArasLabs/project-template-migration/releases/tag/v3.0) | 11.0 SP7, 11.0 SP5
[v2.1](https://github.com/ArasLabs/project-template-migration/releases/tag/v2.1) | 10.0 SP5
[v2.0](https://github.com/ArasLabs/project-template-migration/releases/tag/v2.0) | 10.0 SP5
[v1.0](https://github.com/ArasLabs/project-template-migration/releases/tag/v1.0) | 9.4 SP3

_While this project was built and tested using 11.0 SP15, it should work with any service pack of 11.0._

## Installation

#### Important!
**Always back up your code tree and database before applying an import package or code tree patch!**

### Pre-requisites

1. Aras Innovator installed (version 11.0 SPx preferred)
2. Aras Package Import tool
3. ProjectTemplateMigration import package

### Install Steps

1. Backup your database and store the BAK file in a safe place.
2. Open up the Aras Package Import tool.
3. Enter your login credentials and click **Login**
  * _Note: You must login as root for the package import to succeed!_
4. Enter the package name in the TargetRelease field.
  * Optional: Enter a description in the Description field.
5. Enter the path to your local `..\ProjectTemplateMigration\Import\imports.mf` file in the Manifest File field.
6. Select **ProjectTemplateMigration** in the Available for Import field.
7. Select Type = **Merge** and Mode = **Thorough Mode**.
8. Click **Import** in the top left corner.
9. Close the Aras Package Import tool.

You are now ready to login to Aras and try out the Project Template Migration action.

## Usage

1. Log in to Aras as admin.
2. Navigate to **Templates > Project Templates** in the table of contents (TOC).
3. Search for the Project Template you want to migrate.
4. Right click the Project Template in the main grid and select **GetProjectTemplateAML**.
5. Copy the contents of the dialog.
6. Open up Nash.aspx in a new browser window, or open AML Studio.
7. Enter the credentials for the Aras instance you want to migrate the Project Template to, and click **login**.
8. Paste the Project Template AML and execute it.

Your Project Template will now be available in the target database.

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request

For more information on contributing to this project, another Aras Labs project, or any Aras Community project, shoot us an email at araslabs@aras.com.

## Credits

Original Aras community project written by Aras Corporation Support.

Project rewritten for Aras 11.0 by Chris Borowicz for Aras Support.

Pojrect updated for Aras Innovator 11.0 SP15 by Chris Gillis for Aras Labs.

Documented and published by Eli Donahue for Aras Labs. @elijdonahue

## License

Aras Labs projects are published to Github under the MIT license. See the [LICENSE file](./LICENSE.md) for license rights and limitations.
