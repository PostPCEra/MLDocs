## List various UI & UX samples for inspiration 

### 1. Folder and File menu
- use [codesandbox File menu](https://codesandbox.io/s/kyl0z8yv5?from-embed) as it works well and also good UX.
- code is on [Github](https://github.com/CompuIves/codesandbox-client) -- find which soruce FILE related to "File" menu on scren

- [simple Menu & Caption line on Top](https://javascriptvisualizer.com/?code=function%20bubbleSort%20%28arr%29%20%7B%0A%20%20var%20length%20%3D%20arr.length%3B%0A%20%20var%20swapped%3B%0A%0A%20%20do%20%7B%0A%20%20%20%20swapped%20%3D%20false%3B%0A%0A%20%20%20%20for%20%28var%20i%20%3D%200%3B%20i%20%3C%20length%3B%20i%2B%2B%29%20%7B%0A%20%20%20%20%20%20if%20%28arr%5Bi%5D%20%3E%20arr%5Bi%20%2B%201%5D%29%20%7B%0A%20%20%20%20%20%20%20%20var%20temp%20%3D%20arr%5Bi%5D%3B%0A%20%20%20%20%20%20%20%20arr%5Bi%5D%20%3D%20arr%5Bi%20%2B%201%5D%3B%0A%20%20%20%20%20%20%20%20arr%5Bi%20%2B%201%5D%20%3D%20temp%3B%0A%20%20%20%20%20%20%20%20swapped%20%3D%20true%3B%0A%20%20%20%20%20%20%7D%0A%20%20%20%20%7D%0A%0A%20%20%7D%20while%20%28swapped%29%3B%0A%0A%20%20return%20arr%3B%0A%7D%0A%0AbubbleSort%28%5B5%2C19%2C1%5D%29%3B)
- Sandbox [Client Code ](https://github.com/CompuIves/codesandbox-client/tree/master/packages/app/src/app) as per [this article](https://hackernoon.com/announcing-codesandbox-2-5-be767d15ffd)
- if getting complex get HTML from page "View source" and copy UI and FUncitons.
- **another Option:** use some thing like Jquery FILE/DIr, later see if INd consultant can figure out 'FILE/DIR Menu' of [Stackblitz to extract FILE/DIR code(https://stackblitz.com/edit/react-zbdtps?file=index.js) 

### 2. Folder and File menu 
##### 2.1 Simple File/Folder Menu
- This is Codesandbox Iframe, so it same as above [complex Gitcode base](https://tylermcginnis.com/reactjs-tutorial-a-comprehensive-guide-to-building-apps-with-react/)

##### 2.2 Tabs for Code Editor (Fusion charts)
- top & bottom TABS. Good Top tabs better than plain tabs we saw every where 
- Bottom tabs we can use to as button faces of different versions of code. **such as Ver 1 , Ver 2, Ver 3**
- 'Explore Hover' shows nice compact MENU Options, we can you to show various ML menu options
- FONT size is good, Black theam shows good contrast colour for various Python KEYwords
- screen shot: ![alt text](Top-bottom-Tabs.png)

### 6. single page FAQ or explantation page 
- Recurse FAQ page with [Right hand menu](https://www.recurse.com/manual#sec-environment) : View soruce shows so many &nbsp; etc.. take as it .
- Replace hard code with Mobx/React and generate as Static page. Or use some simple templage language like JINJA
- **Full blown Documentation web site :** If we need full blown , we can use this Reactjs.com Documention CODE on github . Here is [web page](https://reactjs.org/docs/conditional-rendering.html) and the [corrosponding github code](https://github.com/reactjs/reactjs.org/blob/cf628304bb431a0680fc58c577f89dd7cac5b269/content/docs/conditional-rendering.md)

###  7. Chat vs. Forum 
- if Forum then Discourse is way to go. Mostly this will do it. If we need CHAT then seems Zulip is one good one
- Recurse is using Zulip (said on above page), also Zulip mentiond it on Zulip web site

###  8. React ACE Editor Application github repos
- when we need two pane ACE Editors with REACT.js , we can use this ready to use Repo
- For 'Option configuration' we can have it as popup Model window or as Sidebar as shown here : [Sidebar](https://black.now.sh/?version=stable&state=_Td6WFoAAATm1rRGAgAhARYAAAB0L-Wj4ARXAmpdAD2IimZxl1N_WlkPinBFoXIfdFTaTVkGVeHShArYj9yPlDvwBA7LhGo8BvRQqDilPtgsfdKl-ha7EFp0Ma6lY_06IceKiVsJ3BpoICJM9wU1VJLD7l3qd5xTmo78LqThf9uibGWcWCD16LBOn0JK8rhhx_Gf2ClySDJtvm7zQJ1Z-Ipmv9D7I_zhjztfi2UTVsJp7917XToHBm2EoNZqyE8homtGskFIiif5EZthHQvvOj8S2gJx8_t_UpWp1ScpIsD_Xq83LX-B956I_EBIeNoGwZZPFC5zAIoMeiaC1jU-sdOHVucLJM_x-jkzMvK8Utdfvp9MMvKyTfb_BZoe0-FAc2ZVlXEpwYgJVAGdCXv3lQT4bpTXyBwDrDVrUeGOv9m6arhq1vG7gWPofCZzxDVx0XQ0KCGfeks9pc70MAN8zhKZ6WetjhhiFk0PFeo7NMDYe-NfEPd456oNx_KEYz45C3iEE079hLkn6kCYcxJhK3e2MeoPjq1ltI_IjvN_GUYGOGAcLksDFVlmUi-Qk0VTjDc_gzn9wl5Zd1DEs95RC0tBpR1sWvObLHIBZfrKPs047wg-CyszAR-Nh623eoU53wQRTDDzY9w3nG2rVxJNJto5ujL2ARY2w0c0IKUV_WC8HaFUy521komcC_6bE7Uq25H0d__LSj8qaCaFAO9LqMcso3A7tsEpx4-UmXBrUcHibDMQBXm0D1vGkQ8eUljUnR0TMF9NVWy5ntN1T2br3qAWqQK44I8H6kI00gZXWfQIfYHALh7cqfgti0L9Xy3Us2cCsgvD2OioBjVncxYkBm4Y5hVV5g63AAAAAECQA3Mo3QbFAAGGBdgIAACmbK8uscRn-wIAAAAABFla) and it's [github file](https://github.com/jpadilla/black-playground/blob/master/web/components/sidebar.js)
- Here is [index.js](https://github.com/jpadilla/black-playground/blob/master/web/pages/index.js) showing a)sidebar b) editor one c) editor two
```
return (
      <div>
        <Head title="Black Playground" />
        <div className="flex flex-col h-screen">
          <Header version={currentVersion} />

          <div className="flex flex-1 flex-col">
            <div className="flex flex-1 min-h-0">
              <Sidebar
                version={this.state.version}
                versions={this.state.versions}
                options={this.state.options}
                visible={this.state.isSidebarVisible}
                onChange={this.handleOptionsUpdate}
              />

              <div className="flex flex-1">
                <div className="flex flex-1 relative">
                  <Editor
                    value={this.state.source}
                    onChange={this.handleSourceUpdate}
                  />
                </div>
                <div className="flex flex-1 relative">
                  {this.state.isLoading ? (
                    <div className="flex items-center justify-center w-full ace-tomorrow-night">
                      <Spinner />
                    </div>
                  ) : (
                    <Editor value={this.state.formatted} readOnly={true} />
                  )}
                </div>
              </div>
            </div>

```
###  11. general React App : Elegent designs 
 - Githunt app : [website](https://kamranahmed.info/githunt/)  [repo](https://github.com/kamranahmedse/githunt/blob/master/src/components/filters/language-filter/index.js) 
 - so much to learn from this simple React App design (by the same author who did '2018 Webdeveloper' image charts )
 
 
