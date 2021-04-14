# Integration Theme Example:  Styling with CSS
### Version: 1.0.0
#### Minimum DriveWorks Version: 18.0

A distributable example that demonstrates how to style DriveWorks controls using CSS.

Please note: DriveWorks are not accepting pull requests for this example.  
Join our [online community](https://my.driveworks.co.uk) for discussion, resources and to suggest other examples.

### This example:
- Demonstrates using basic metadata & CSS selectors, and further advanced styling that CSS enables.
- Provides 2 DriveWorks Packages (.drivepkg), each containing an example Project that demonstrate use of the Metadata property and styling various properties.
    - **BasicStyles18.drivepkg** - Demonstrates using metadata & basic CSS selectors to target DriveWorks controls (see also: /basic-styles/style.css)
    - **AdvancedStyles18.drivepkg** - Demonstrates some possibilities for advanced styling made available via CSS (see also: /advanced-styles/advanced-styles.css)

The CSS selectors/styles demonstrated can be viewed without installing the provided Projects, for quick reference. Simply open the included `.css` files.

### /basic-styles

![Basic Example](/images/basic.png)

- Creates a new Specification
- Loads in a custom stylesheet (/basic-styles/style.css)
- Styles a single button control - using the Project 'BasicStyles18'
- Demonstrates:
    - Targeting controls with the `Metadata` property (data-metadata)
    - Using CSS Attribute Selectors
    - Rounded Corners (border-radius)
    - Shadows (box-shadow)
    - Animating styles (transition)
    - Rotate and Scale (transform)
    - Gradients (linear-gradient)
    - Hover styles (:hover)
    - Styling child elements

### /advanced-styles

![Advanced Example](/images/advanced.png)

- Creates a new Specification
- Loads in an alternate custom stylesheet (/advanced-styles/advanced-styles.css)
- Styles multiple controls - using the Project 'AdvancedStyles18'
- Demonstrates:
    - Various button styles
    - CSS Transforms (rotate/scale/skew)
    - CSS Filters (blur, grayscale)
    - Animating position changes

### To use:
1. Clone this repository, or download as a .zip

2. Extract each of the supplied .drivepkg files using the DriveWorks Package Wizard to access the included Project files.

3. Open the extracted Groups in DriveWorks Administrator and use 'Form Design' to view each Controls and its properties.
    * Most importantly: the 'Metadata' properties that are targeted via CSS.

4. In `DriveWorksLiveConfigUser.xml`, add a new Group Alias for the each new Group containing the example Projects.
    * See [Integration Theme Settings](https://docs.driveworkspro.com/Topic/IntegrationThemeSettings) for additional guidance.

5. Open the extracted Groups in DriveWorks Live and start the Integration Theme.
    * See [Selecting the Integration Theme](https://docs.driveworkspro.com/Topic/IntegrationThemeSelect) for additional guidance.

6. Enter your Integration Theme details into `config.js` for each example.
    * `serverUrl` - The URL that hosts your Integration Theme, including any ports.
    * `groupAlias` - The public alias created for the Group containing the DriveApps to render - as configured in DriveWorksConfigUser.xml.
        * This *must* be specified for each Group you wish to use.
        * This allows you to mask the true Group name publicly, if desired.
        * See [Integration Theme Settings](https://docs.driveworkspro.com/Topic/IntegrationThemeSettings) for additional guidance.
    * `projectName` - The name of the Project to render a Specification from.
        * These are pre-filled with supplied Project names, but can be changed if required.

7. Open the example HTML files locally (localhost) or on a remote server.
    * Ensure `<corsOrigins>` in DriveWorksConfigUser.xml permits request from this location.
    See [Integration Theme Settings](https://docs.driveworkspro.com/Topic/IntegrationThemeSettings) for additional guidance.

8. If encountering any issues, check the browser's console for error messages (F12)

### Potential Issues:
* When serving this example for a domain different to your DriveWorks Live server, e.g. api.my-site.com from company.com, 'SameSite' cookie warnings may be thrown when the Client SDK attempts to store the current session id.
    * This appears as "Error: 401 Unauthorized" in the browser console, even with the correct configuration set. 
    * To resolve:
        * Ensure you are running DriveWorks 18.2 or above, HTTPS is enabled in DriveWorks Live's settings and a valid SSL certificate has been configured via DriveWorksConfigUser.xml.
        * See [Integration Theme Settings](https://docs.driveworkspro.com/Topic/IntegrationThemeSettings) for additional guidance.

---

This source code has been made available to demonstrate how you can integrate with DriveWorks using the DriveWorks Live API.
This code is provided under the MIT license, for more details see LICENSE.md.

The example requires that you have the latest DriveWorks Live SDK installed, operational and remotely accessible.
