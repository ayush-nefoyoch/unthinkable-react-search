# unthinkable-react-search
### A ReactJS component to render a searching and pagination.
> By using this component, get all the functionalities which are related to pagination and searching by passing a small amount of data.
>> You can get the default styling or you can add the styling which you want.


## Installation 
1. Clone the repository - **[Clone Repo from here](https://github.com/nefoyoch/unthinkable-react-search)**
2. run `npm i`
3. run `npm link`
4. run `npm link ../path/to/your/project/node_modules/react`

> Now, in the project in which you want to use this package -
- run `npm link unthinkable-react-search` 
- run `npm start`

## Usage
```JSX
import { ReactSearch } from "unthinkable-react-search"
```
> *Get the default styles by passing data as props* - 
   ```JSX
   <ReactSearch
      endpoint={<API>
      tableType={<TABLETYPE>}
      isSearchResults={true}
      isPagination={true}}
   />
   ```
![Home](assets/images/Home.png)

#### Customize the Package with Props

|      Name                      |             Type       | Description                                            |
| -------------------------------| ----------------| --------------------------------------------------------------                                  
|     `endPoint`                 |     `String`    | **Required**. API for fetching data which is to be displayed.  |
|     `tableType`                |     `String`    | **Required**. Type of the table `e.g. users/students`          |
|     `isSearchResults`          |     `Boolean`   | **Required**. To display Search Results. `Pass value as false if not required.`|
|     `isPagination`             |     `Boolean`   | **Required**. To get functionalities of pagination. `Pass value as false if not required.`| 
|     `defaultPageSize`          |     `Number`    |   Number of rows to be displayed. `default: 5`|
|     `pageSizeOptions`          |     `Array`     |   Items to be displayed on dropdown menu `default: [5, 10, 15, 20]`, if not required do not write this prop.         |
|     `searchPlaceholderText`    |     `String`    |   Text to be displayed on Search Bar. `default: Search...`|
|     `omittedHeaders`           |     `Array`     |   Headers which you do not want to be displayed.|
|     `tableStyling`             |     `Object`    |   Styles of the table to be displayed.|
|     `searchIconVariant`        |     `String`    |   Color of a Search Bar Icon `default: secondary`.|
|     `dropDownVariant`          |     `String`    |   Color of a Drop-Down menu. `default: primary`|
|     `paginateBtnVariant`       |     `String`    |   Color of pagination buttons. `default: outline-primary`|
|     `dateTimeFormat`           |     `String`    |   Format of date & time (if present). `default: MMMM DD YYYY, h:mm:ss a`|

* endPoint - **API Format**
> e.g.
```JSON
{
   "users":{
      "current_page":1,
      "data":[
         {
            "id":316,
            "firstname":"Rt",
            "surname":"We",
            "company_name":"Prachi.gupta+t1@unthinkable.co",
            "email":"ae@wef.sd",
            "currency":"pound",
            "created_at":"2021-09-08T09:22:21.000000Z",
            "fullname":"Rt We",
            "plan_status":"Expired",
            "owner_id":0,
            "active_subscription":null,
            "group":null
         }
      ],
      "first_page_url":"https://divisus-admin.cloudzmall.com/api/unthinkable/search?q=sd&per_page=1&table=users&page=1",
      "from":1,
      "last_page":1,
      "last_page_url":"https://divisus-admin.cloudzmall.com/api/unthinkable/search?q=sd&per_page=1&table=users&page=1",
      "links":[
         {
            "url":null,
            "label":"&laquo; Previous",
            "active":false
         },
         {
            "url":"https://divisus-admin.cloudzmall.com/api/unthinkable/search?q=sd&per_page=1&table=users&page=1",
            "label":"1",
            "active":true
         },
         {
            "url":null,
            "label":"Next &raquo;",
            "active":false
         }
      ],
      "next_page_url":null,
      "path":"https://divisus-admin.cloudzmall.com/api/unthinkable/search",
      "per_page":1,
      "prev_page_url":null,
      "to":1,
      "total":1,
      "keys":[
         "id",
         "firstname",
         "surname",
         "company_name",
         "email",
         "currency",
         "created_at"
      ]
   }
}
```
> **NOTE** -  *Refer to React Bootstrap for styling purpose*.
* *tableStyling*: 
   > e.g. 
   
   
   ```JSX
            tableStyling={{
               size: "",
               variant: "",
               bordered: <boolean>,
               striped: <boolean>,
               hover: <boolean>,
            }}
    ```

   > `size: "md"/"sm"` `default: ""`


   > `variant: "dark"/""` `default: ""` 

> *Passing all props in a component* - `e.g.`

```JSX
  <ReactSearch
      endPoint={<API>}
      tableType={<TABLE>}
      defaultPageSize={<DEFAULT_PAGE_SIZE>}
      pageSizeOptions={<PAGE_SIZE_OPTIONS>}
      isSearchResults={true}
      isPagination={true}
      searchPlaceholderText="Search Me"
      omittedHeaders={["currency", "created_at"]}
      tableStyling={{
        size: "sm",
        variant: "dark",
        bordered: true,
        striped: true,
        hover: false,
      }}
      searchIconVariant="success"
      dropDownVariant="success"
      paginateBtnVariant="outline-success"
      dateTimeFormat="MMMM Do YYYY"
  />
```
   > *Now it looks like* - 

![Pagination and Searching Home Page](/assets/images/WithProps.png)


## Credits 
   #### Collaborators
      Neelkanth Kaushik - `<gihub profile link>`
      Tanveer Kaur - `<gihub profile link>`
      
      
## License
 
 


