# Testing with playwright-browserstack in C#

[Playwright](https://playwright.dev/dotnet/) Integration with BrowserStack.

![BrowserStack Logo](https://d98b8t1nnulk5.cloudfront.net/production/images/layout/logo-header.png?1469004780)

## Setup

* Clone the repo and run `cd csharp-playwright-browserstack`
* Set `BROWSERSTACK_USERNAME` and `BROWSERSTACK_ACCESS_KEY` as environment variables with your [BrowserStack Username and Access Key](https://www.browserstack.com/accounts/settings)
* Run `dotnet build`

## Running your tests

- To run a single test, run `dotnet run single`
- To run a parallel test, run command `dotnet run parallel`
- To run sessions on emulated devices, 
`dotnet run iphonetest` or `dotnet run pixeltest`
You can specify any device name from the below list: 
https://github.com/microsoft/playwright/blob/main/packages/playwright-core/src/server/deviceDescriptorsSource.json

  ### Run sample test on privately hosted websites

    **Using Command-line Interface**
    1. You have to download the BrowserStack Local binary from the links below (depending on your environment):
        * [OS X (10.7 and above)](https://www.browserstack.com/browserstack-local/BrowserStackLocal-darwin-x64.zip)
        * [Linux 32-bit](https://www.browserstack.com/browserstack-local/BrowserStackLocal-linux-ia32.zip)
        * [Linux 64-bit](https://www.browserstack.com/browserstack-local/BrowserStackLocal-linux-x64.zip)
        * [Windows (XP and above)](https://www.browserstack.com/browserstack-local/BrowserStackLocal-win32.zip)
    2. Once you have downloaded and unzipped the file, you can initiate the binary by running the command: `./BrowserStackLocal --key YOUR_ACCESS_KEY`
    3. Once you see the terminal say "[SUCCESS]" You can now access your local server(s) in our remote browser”, your local testing connection is considered established.
    4. You can then run the sample Local test using `dotnet run local`


## Notes
* You can view your test results on the [BrowserStack Automate dashboard](https://www.browserstack.com/automate)

## Additional Resources
* [Documentation for writing Automate test scripts with BrowserStack](https://www.browserstack.com/docs/automate/playwright)
