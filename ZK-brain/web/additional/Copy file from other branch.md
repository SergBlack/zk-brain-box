202209061034
Tags: #web

--- 
# Copy file from other branch
To copy file you need to know branch name and file path.

Command:
```js
git restore --source <branch> -- <filepath1 filepath2 ... filepathN>
```

Example
```js
git restore --source feat/UE-6618-denver-conditional-data-selector -- packages/web/src/pages/productDetails/components/DenverProductPlansSection/utils/getFilteredPlans/getFilteredPlans.ts
```

--- 
### Links
- [[]]