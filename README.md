<p align="center" style="text-align:center">
    <img src="./illustration.svg" alt="illustration" width="100"/>
</p>

# Smart-grid generator

> Layout script which generate smart grid from package.json 

### Install

```shell
npm i smart-grid
```

### Initialization

* Download script to dir which contain package.json

```shell
wget https://github.com/webster6667/smart-grid-generator-layout/master/smart-grid.js
```

* Add script to package.json

```json
{
  "name": "package-name",
  "version": "0.0.1",
  "scripts": {
    "build-grid": "node smart-grid.js"
  }
}
```

* Fill smart-grid.js config

* Run npm script
```shell
npm run build-grid
```

#### Smart-grid config description
* `smartGrid(outputPathForGenerateFile, config)`
* **Columns:** number of grid columns
* **Offset**: offset for one side of column and negative offset one of row side `(px || % || rem)`
  * **Example**: if `offset: '10px'`, space between column will be `20px`, negative offset of row left/right will be `-10px`
* **MobileFirst**: `mobileFirst === true ? 'min-width' : 'max-width'`

* **Container**
    * **Fields**: size one of secure fields
    * **MaxWidth**:  `max-width` for container with secure fields
        * **Example**: if `maxWidth: '1920px'` max content size will be `1880px`, `40px` will be secure fields
## Author

webster6667
