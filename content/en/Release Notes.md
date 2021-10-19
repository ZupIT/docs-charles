---
title: Release Notes
weight: 98
description: In this section, you will find CharlesCD Release Notes.
---

{{% release/group %}}

{{% release/item type="feature" date="May 2021" %}}

Create CI/CD for staging.

Update helm values.yaml.

Increase default timeout time.

CI Update of charts and changelog.

Update release pipeline.
{{% /release/item %}}
 
{{% release/item repository="Butler" date="May 2021" %}}
Add Butler operator.

Add Butler events logs aggregator.

Charlescd release 1.0.0.

Add notification on module deletion.

Add undeploy moove notification.

Sort logs by date.
{{% /release/item %}} 

{{% release/item repository="UI" date="May 2021" %}}
Add clipboard support for HTTP protocol.

Add max length validation to input fields.

Update routing when account is clicked.

Show notification on delete.

Add new endpoint to find simplified circle data.

Show notification on delete a webhook.

Add validation isNotBlank for Workspaces' name on creation.

Add responsiveness to change password modal.

Add margin for subtitle in editing mode.

Add minLength to workspace description.
{{% /release/item %}}

{{% release/item repository="GATE" date="May 2021" %}}
Add workspace id to authorize request and log deny request.

Add System Token.

Add notification on module deletion.

Add deployment config field.
{{% /release/item %}}

{{% release/item repository="MOOVE" date="May 2021" %}}
Charlescd: release 0.7.1.

Add deployment active on patch workspace to remove deployment config.

Add validation when delete configuration to active deployments.
{{% /release/item %}}

{{% release/item repository="MOOVE" date="April 2021" %}}
Add deploy logs.
Sync circle matcher information when creating or deleting.
{{% /release/item %}}

{{% release/item repository="UI" date="April 2021" %}}
Add Webhook module.
Sync circle matcher information when creating or deleting.
Add which Charles version.
{{% /release/item %}}

{{% release/item repository="Butler" date="April 2021" %}}
Add percentage deployment strategy.
{{% /release/item %}}


{{% release/item type="fix" repository="UI" date="May 2021" %}}
Bump ssri from 6.0.1 to 6.0.2 in /ui.

Fix usergroup modal.

Fix module and components options.

Fix typos and item layout.

Fix namespaced deployment.

Fix workspace refresh menu.

Fix action circle list.

Fix user group permission and create a modal for user group removal.

Fix build error and save action.

Fix UI webhook.

Fix vertical align for InputTitle.

Fix metric action.

Fix defaultValue for Account Profile.

{{% /release/item  %}}

{{% release/item repository="Moove" date="May 2021" %}}
Auth and token is now nullable.

Fix system token test that was broken by the deployment logs service update.

Improve moove error message.

Fix matcher csv update.

Handle template error.

Fix deployment configuration validation on workspace update.

Fix user deletion from user group.

Fix configuration delete validation.

Fix count query.

Fix execution time value.

Fix error message.

Fix usergroup name edit.

Fix semver version from csv validator.

Fix CSV validator version.

Fix matcher update.

Fix workspace status.
{{% /release/item  %}}

{{% release/item date="May 2021" %}}
Fix enabling gate configurations at values.yaml.

Fix helm install v1.0.

Fix permissions by workspace query.

Fix cluster role for butler adding access for all API groups.

Fix the pipeline.

Fix update on authorize.

Fix chart.
{{% /release/item  %}}

{{% release/item repository="Butler" date="May 2021" %}}
Bump y18n from 4.0.0 to 4.0.3 in /butler.

Fix git error.

Changed token, gatewayName and host value validation.

Fix log endpoint.

Handle template error. 

Hotfix/moove request git token base64.

Fix error when helm url is invalid.

Fix namespace override "deadlock".

Fix cache error.

Fix lint error and send UNDEPLOY_FAILED by default.

Fix error messages.

Fix usergroup name edit.
{{% /release/item  %}}

{{% release/item repository="Moove" date="May 2021" %}}
Remove the 'created' option the from permission struct.

Fix system token regenerate.

Fix regen system token.

Fix wrong method on policies csv.
{{% /release/item  %}}

{{% release/item repository="UI" date="April 2021" %}}
Fix [UserGroups] Prevent duplicate list after updates.

Fix button enabled/disabled when creating a new user.

Fix circle creation from CSV file.

[UserGroups] Permission to Maintainer remove Groups from Workspace.

Fix showing username undefined in the initial screen.

Fix inconsistently displaying the menu after go to root path.

Fix showing required for an optional field when registering a module.

{{% /release/item  %}}

{{% release/item repository="Butler" date="April 2021" %}}
Change Butler steps on the pipeline.

{{% /release/item  %}}

{{% release/item repository="Moove" date="April 2021" %}}
Fix getting circle percentage at the repository.

{{% /release/item  %}}

{{% release/item repository="Compass" date="April 2021" %}}
 Fix list metric prometheus error.

{{% /release/item  %}}

{{% release/item repository="Hermes" date="April 2021" %}}
 Fix list metric prometheus error.

{{% /release/item  %}}

{{% release/item type="chore" repository="UI" date="May 2021" %}}
UI Operator.

Remove legacy code and infinite scroll.

Change UI package manager from yarn to npm.

Change text in button.

Test useUpdateName exception.

Improve text of button in token creation.

Update the user menu after modifying any user.

Disable button on deploy.

Update user menu by changing the name.

Change isNotBlank text from 'No whitespace' to 'Cannot start with whitespaces'.

Set modules branch field as not required.

Upgrade Wizard.
{{% /release/item  %}}

{{% release/item repository="Moove" date="May 2021" %}}
Remove unnecessary id from log response.

Delete deployment configuration.

Enhancement/duplicated entities.

Update Keycloak version.

Change logs set to List to garantee order.

Delete default root user.

Overrides csv validator dependencies.
{{% /release/item  %}}

{{% release/item repository="Gate" date="May 2021" %}}
Update policy adding workspace post to management role.

{{% /release/item  %}}

{{% release/item repository="Butler" date="May 2021" %}}
Validate uppercase tags.

Setting butler request size limit for 50mb by default.

Bump lodash from 4.17.19 to 4.17.21 in /butler.
{{% /release/item  %}}

{{% release/item repository="Villager" date="May 2021" %}}
Remove unused villager dependency.

{{% /release/item  %}}

{{% release/item date="May 2021" %}}
Update envvar skip SSL.

Upgrade CI trigger for bug-hunting.
{{% /release/item  %}}

{{% release/item repository="UI" date="April 2021" %}}
Remove hypotheses feature.
Improve advanced options at component screen.
Remove actions from module tab when creating it.
Upgrade react-scripts from 4.0.1 to 4.0.3.
Add Mock Service Worker on UI.
Bump node-notifier from 8.0.0 to 8.0.1 in /ui.
 Bump elliptic from 6.5.3 to 6.5.4 in /ui.
{{% /release/item  %}}

{{% release/item repository="Butler" date="April 2021" %}}
Butler executions filters.
{{% /release/item  %}}

{{% release/item type="docs" date="October 2021" %}}
 Documentation migration from Gitbook to Hugo. 
  
  Fix documentation links.
  {{% /release/item  %}} 

{{% /release/group %}}

Access CharlesCD [**Release Notes page**](https://github.com/ZupIT/charlescd/releases).
