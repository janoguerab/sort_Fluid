# sort_Fluid
This Repo is just information about How to add sortin with Fluid in typo3:

1. Install with composer flux : composer req fluidtypo3/flux
2. Install with composer vhs  : composer req fluidtypo3/vhs
3. Enable the extensions Flux and VHS in the Extension Manager.
4. To remove the message "Please select a page template in page properties." - Add in the Template, at the setup part: 
 ```typoscript
 page.5 >
 ```
5. Add in the html the view Helpers: 
```html
  {namespace flux=FluidTYPO3\Flux\ViewHelpers}
  {namespace v=FluidTYPO3\Vhs\ViewHelpers}
```
6. Finally use vhs in a foreach : 
```html
<f:for each="{professors -> v:iterator.sort(sortBy: 'firstName')}" as="professor">
</f:for>
```

Other examples and information in the [oficial page](https://fluidtypo3.org/viewhelpers/vhs/master.html)
