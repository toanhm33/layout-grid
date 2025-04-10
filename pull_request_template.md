## Checklist


### Structure FE features
[ ] 1. src/app/layout interact to all providers (Root layout)
[ ] 2. src/app/(modules)/layout to share across app (AppShell layout)
[ ] 3. Use DetailFormLayout|DetailTableLayout (Content layout)
js
src/app/layout
const abc = () => {
    
}
-----
src/app/(modules)/layout
const xyz = () => {
    
}
----
Content layout
const qwe = () => {
    
}

#### Common
[ ] Import from alias. Example **@app**
[ ] File name follow **main-layout.tsx** . Component **MainLayout**

#### Type
[ ] AVOID use type any
[ ] NOT put type to types folder
[ ] If type not much, put it inside the component
[ ] If type much, put it inside new file at same level of FC


#### Style
[ ] SCSS file inside the folder /scss
[ ] Must use Mantine, use **Mantine props** to style (If props doesn't support, use SCSS)
[ ] Use color follow **mies-portal.theme.ts**. Please refer to (Mantine theme)[https://mantine.dev/theming/colors/] (spacing)[https://mantine.dev/styles/css-variables/]
[ ] Use React-icons


#### API
[ ] React Query - create custom hooks for calling API. **useGetUserDataQuery** and put into lib/data/(folder-name)/hooks
[ ] **NOT put api call into services** anymore as it will be remove, put it into lib/data/(folder-name)
[ ] Server component data to client => **use hydrate** method instead of initialData

#### Git
[ ] Branch name: Example **feat-MP-66-2FA-for-AD-login** if have task ID OR **feat-incident-detail-page** without task ID
