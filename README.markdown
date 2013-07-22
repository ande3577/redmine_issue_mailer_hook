# redmine_issue_mailer_hook

Master branch works on redmine 2.4.x ONLY. 2.3.x must use 2.3-branch.

## Overview

This plugin adds a pair of view hooks to the issue mailer.  This enables a 
plugin to add additional fields to the issue e-mail notification.

Currently the following hooks are provided (all provide the issue as context).

* view_issues_mailer_after_url - below the issue URL at the top of the 
notification email
* view_issues_mailer_after_fields - the end of the fields list
* view_issues_mailer_after_description - after the description

To implement the hook, add the following to your hooks file:

    render_on :view_issues_mailer_after_fields, :partial => 'mailer/plugin_issue_hook'
    
Then implement a view for both _plugin_issue_hook.text.erb and 
_plugin_issue_hook.html.erb

## Installation

1. Clone the plugin the plugins directory.
2. Restart the server

## License

This program is free software: you can redistribute it and/or modify 
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.


