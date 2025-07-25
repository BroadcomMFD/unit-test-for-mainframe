<div id="header" align="center">

[![Code4z](https://img.shields.io/badge/Code4z-marketplace-cc092f)](https://marketplace.visualstudio.com/search?term=code4z&target=VSCode)

</div>

# Unit Test for Mainframe

Unit Test for Mainframe brings the capabilities of Test4z into your VS Code development environment. Test4z provides capabilities for unit testing, record and replay testing, and code coverage metrics on user mainframe applications. Test4z is built to work with any programming language (such as COBOL, PL/I, C, or Assembler) that produces a mainframe load module. Test4z provides the most benefit for COBOL programs.

The extension includes the following features:
- Execute unit tests
- View code coverage metrics
- Use code snippets to add sample code for the Test4z COBOL API 

<br/>

<img align="left" alt="This extension is part of the Code4z experience" width="80" height="82" src="https://raw.githubusercontent.com/BroadcomMFD/code4z/refs/heads/main/icon5.png" />

Unit Test for Mainframe is part of the [Code4z](https://techdocs.broadcom.com/code4z) experience from Broadcom, which offers a modern experience for mainframe application developers. To get started with Code4z, check out our foundational [extension pack](https://marketplace.visualstudio.com/items?itemName=broadcomMFD.code4z-extension-pack).

<br/>

## Address Software Requirements

  - VS Code 1.77.0 or higher.
  - Test4z, including the Command Line Interface (part of the npm package, refer to the _Install Test4z Command Line Interface_ section in the [Test4z documentation](https://techdocs.broadcom.com/test4z)).
  - A COBOL LSP is required to use the Test4z VS Code snippets. Install [COBOL Language Support](https://marketplace.visualstudio.com/items?itemName=broadcomMFD.cobol-language-support) or the Code4z foundational [extension pack](https://marketplace.visualstudio.com/items?itemName=broadcomMFD.code4z-extension-pack). For more information on configuring the COBOL LSP, see _COBOL Language Support Configuration_ in the _Using the VS Code Extension_ section in the [Test4z documentation](https://techdocs.broadcom.com/test4z).

Verify the installation of VS Code and Test4z from the CLI:

```
code --version
t4z --version
```

## Compatibility

Unit Test for Mainframe is supported on Visual Studio Code.

We recommend the use of [Zowe Explorer](https://marketplace.visualstudio.com/items?itemName=Zowe.vscode-extension-for-zowe) to access mainframe data sets in connection with your testing activities. You can use Zowe Explorer to submit JCL or to edit the recorded data. Zowe Explorer is available as part of the Code4z foundational [extension pack](https://marketplace.visualstudio.com/items?itemName=broadcomMFD.code4z-extension-pack). The Unit Test for Mainframe extension works seamlessly with the Code4z foundational extension pack for z/OS application developers.



## Using the Extension

### Project Initialization

To initialize a project, perform the following steps from the VS Code menu:

1. Click **File > Open Folder...** to select and open your folder.

2. Click **View > Command Palette...** to open the VS Code Command Palette. Select **Test4z Initialize**.

3. Respond to the prompts to complete the initialization. If needed, see the _Initialize the Project_ section in the [Test4z documentation](https://techdocs.broadcom.com/test4z).


### Execute Unit Tests

Test4z allows you to run all tests or to run individual tests. In either case, you can choose to run with or without code coverage.

#### Run all tests:

1. Right-click the **test** directory. 
A context menu appears. 

2. Select **Test4z Run All Tests** to run the complete set of tests.

    _or_

    Select **Test4z Run All Tests with Coverage** to run the tests along with code coverage analysis.

#### Run individual tests:

1. In the **test** directory, navigate to a specific test file and right-click the file.

2. Select **Test4z Run Test** for a standard test run.

    _or_

    Select **Test4z Run Test with Coverage** to run the test along with code coverage analysis.


### View Code Coverage Metrics

To analyze code coverage in your project, perform the following steps:

#### Access Coverage Dashboard

1. Execute your tests with the coverage option enabled. The `coverage` folder is created.

2. Right-click the `coverage` folder and select **Test4z Open Coverage Dashboard**. This action opens the Code Coverage panel.

3. In the Code Coverage panel, click any program to visualize code coverage at the source code level.

#### View Detailed Coverage Metrics for COBOL Source Code

1. Execute your tests with the coverage option enabled. The `coverage` folder is created.

2. From the `src` folder, open the specific COBOL source file that you want to examine. The code coverage information is displayed in the editor.

![Coverage Dashboard](https://raw.githubusercontent.com/BroadcomMFD/unit-test-for-mainframe/main/GIF/CoverageDashboard.gif)

#### Integrating Coverage Reports into CI/CD Pipelines

If you want to publish code coverage reports within your CI/CD pipeline, multiple report formats are readily available within the generated `coverage` folder.

### Code Snippets

Unit Test for Mainframe provides COBOL code snippets that make it faster and easier to create your unit tests. Most of the code snippets directly correspond to the Test4z COBOL APIs. For more information on the Test4z COBOL APIs, see the _COBOL API_ section in the [Test4z documentation](https://techdocs.broadcom.com/test4z).

Some snippets contain comments or highlighted variables to assist in customizing the sample code for your test program.

Find and select a snippet:

1. In your COBOL test program, type **t4z** to view the available snippets. You can also click **View > Command Palette > Snippets: Insert Snippet** from the VS Code menu.

2. Type additional keywords, like the API name, to narrow the results. The highlighted snippet displays a short description, along with the COBOL code to insert.

3. Select the desired snippet. The code sample is copied to your test program.

![Code Snippets](https://raw.githubusercontent.com/BroadcomMFD/unit-test-for-mainframe/main/GIF/CodeSnippets.gif)


## License

The Unit Test for Mainframe VS Code extension is made available to customers on the Visual Studio Code Marketplace in accordance with the terms and conditions contained in the provided End-User License Agreement (EULA).


## Privacy Notice

In the event that Broadcom needs to process your personal data this is done in accordance with Broadcom’s [Privacy Notice](https://www.broadcom.com/company/legal/privacy/policy).

## Technical Assistance and Support

The Unit Test for Mainframe extension is made available to customers on the Visual Studio Code Marketplace in accordance with the terms and conditions contained in the provided End-User License Agreement (EULA).

If you are on active support for Test4z, you get technical assistance and support in accordance with the terms, guidelines, details, and parameters that are located within the Broadcom [Working with Support](https://support.broadcom.com/external/content/release-announcements/CA-Support-Policies/6933) guide.

This support generally includes:

* Telephone and online access to technical support
* Ability to submit new incidents 24x7x365
* 24x7x365 continuous support for Severity 1 incidents
* 24x7x365 access to Broadcom Support
* Interactive remote diagnostic support
* Technical support cases must be submitted to Broadcom in accordance with guidance provided in “Working with Support”.

Note: To receive technical assistance and support, you must remain compliant with “Working with Support”, be current on all applicable licensing and maintenance requirements, and maintain an environment in which all computer hardware, operating systems, and third party software associated with the affected Broadcom software are on the releases and version levels from the manufacturer that Broadcom designates as compatible with the software. Changes you elect to make to your operating environment could detrimentally affect the performance of Broadcom software and Broadcom shall not be responsible for these effects or any resulting degradation in performance of the Broadcom software. Severity 1 cases must be opened via telephone and elevations of lower severity incidents to Severity 1 status must be requested via telephone.


---

Copyright © 2025 Broadcom. The term "Broadcom" refers to Broadcom Inc. and/or its subsidiaries.
