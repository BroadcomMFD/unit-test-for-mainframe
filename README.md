# Unit Test for Mainframe

## Introduction

The Unit Test for Mainframe VS Code extension brings the capabilities of Test4z into your VS Code development environment. Test4z provides capabilities for unit testing, record and replay testing, and code coverage metrics on user mainframe applications. Test4z is built to work with any programming language (such as COBOL, PL/I, C, or Assembler) that produces a mainframe load module. Test4z provides the most benefit for COBOL programs.

The extension includes the following features:
- Execute unit tests
- View code coverage metrics
- Use code snippets to add sample code for the Test4z COBOL API 

## Prerequisites

  - VS Code 1.77.0 or higher
  - Test4z including the Command Line Interface (part of the npm package, refer to the _Install Test4z Command Line Interface_ section in the [Test4z documentation](https://techdocs.broadcom.com/test4z))

Verify their installation from the CLI:

```
code --version
t4z --version
```

## Compatibility

Unit Test for Mainframe is supported on Visual Studio Code.

We recommend the use of [Zowe Explorer](https://marketplace.visualstudio.com/items?itemName=Zowe.vscode-extension-for-zowe) to access mainframe data sets in connection with your testing activities. You can use Zowe Explorer to submit JCL or to edit the recorded data. Zowe Explorer is available as part of the [Code4z](https://marketplace.visualstudio.com/items?itemName=broadcomMFD.code4z-extension-pack) package. The Unit Test for Mainframe extension works seamlessly with the Code4z extension pack for z/OS application developers.



## Using the Extension

### Project Initialization

To initialize a project, perform the following steps from the VS Code menu:

1. Click **File > Open Folder...** to select and open your folder.

2. Click **View > Command Palette...** to open the VS Code Command Palette. Select **Test4z Initialize**.

3. Respond to the prompts to complete the initialization. If needed, see the _Initialize the Project_ section in the Test4z documentation.


### COBOL Language Support Configuration

To use the Test4z code snippets, a COBOL LSP is required. Install Broadcom's [COBOL Language Support](https://marketplace.visualstudio.com/items?itemName=broadcomMFD.cobol-language-support) or the complete [Code4z](https://marketplace.visualstudio.com/items?itemName=broadcomMFD.code4z-extension-pack) package. You can configure the COBOL LSP to find the Test4z COBOL API copybooks. This helps with syntax checking of the code and navigation to the copybooks.

The `t4z init` command creates the file `.vscode/settings.json` with the following content:

```json
{
  "cobol-lsp.cpy-manager.paths-local": [
    "<path to the Test4z>/cobol_api/cpy"
  ]
}
```

If you want to add the path to the Test4z COBOL API copybooks into an existing configuration, perform the following steps:

1. Find the path to Test4z:

    ```
    t4z home
    ```

2. Update the value of the `cobol-lsp.cpy-manager.paths-local` property in the `.vscode/settings.json` or _cobol-lsp_ - _Cpy-manager:
Paths-local_ in the VS Code Settings (**File > Preferences > Settings**) so it contains `"<path to the Test4z>/cobol_api/cpy"`.

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

![Coverage Dashboard](https://github.com/BroadcomMFD/unit-test-for-mainframe/blob/main/GIF/CoverageDashboard.gif)

#### Integrating Coverage Reports into CI/CD Pipelines

If you want to publish code coverage reports within your CI/CD pipeline, multiple report formats are readily available within the generated `coverage` folder.

### Code Snippets

The Unit Test for Mainframe VS Code extension provides COBOL code snippets that make it faster and easier to create your unit tests. Most of the code snippets directly correspond to the Test4z COBOL APIs. For more information on the Test4z COBOL APIs, see the `COBOL API` section in the [Test4z documentation](https://techdocs.broadcom.com/test4z)

Some snippets contain comments or highlighted variables to assist in customizing the sample code for your test program.

Find and select a snippet:

1. In your COBOL test program, type **t4z** to view the available snippets. You can also click **View > Command Palette > Snippets: Insert Snippet** from the VS Code menu.

2. Type additional keywords, like the API name, to narrow the results. The highlighted snippet displays a short description, along with the COBOL code to insert.

3. Select the desired snippet. The code sample is copied to your test program.

![Code Snippets](https://github.com/BroadcomMFD/unit-test-for-mainframe/blob/main/GIF/CodeSnippets.gif)


### License

The Unit Test for Mainframe VS Code extension is made available to customers on the Visual Studio Code Marketplace in accordance with the terms and conditions contained in the provided End-User License Agreement (EULA).


### Privacy Notice

In the event that Broadcom needs to process your personal data this is done in accordance with Broadcom’s [Privacy Notice](https://www.broadcom.com/company/legal/privacy/policy).

### Technical Assistance and Support

If you are on active support for Test4z, you may be entitled to technical assistance and support in accordance with the terms of your agreement and Broadcom's support policies.

---

Copyright © 2024 Broadcom. The term "Broadcom" refers to Broadcom Inc. and/or its subsidiaries.
