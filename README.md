# mapshaper

### Introduction

Mapshaper is software for editing Shapefile, GeoJSON, [TopoJSON](https://github.com/mbostock/topojson/wiki), CSV and several other data formats, written in JavaScript.

The `mapshaper` command line program supports essential map making tasks like simplifying shapes, editing attribute data, clipping, erasing, dissolving, filtering and more.

The web UI supports interactive simplification, attribute data editing, and running cli commands in a built-in console. Visit the public website at [www.mapshaper.org](http://www.mapshaper.org) or use the web UI locally via the `mapshaper-gui` script.

See the [project wiki](https://github.com/mbloch/mapshaper/wiki) for more documentation on how to use mapshaper.

To suggest improvements, add an [issue](https://github.com/mbloch/mapshaper/issues).

To learn about recent updates, read the [changelog](https://github.com/mbloch/mapshaper/releases).

### Command line tool

The `mapshaper` command line program has been used successfully under Mac OS X, Linux and Windows.

The project wiki has an [introduction](https://github.com/mbloch/mapshaper/wiki/Introduction-to-the-Command-Line-Tool) to using the command line tool that includes many simple examples.

For a detailed reference, see the [Command Reference](https://github.com/mbloch/mapshaper/wiki/Command-Reference).



### Interactive web interface

The web UI works in recent desktop versions of Chrome, Firefox, Safari and Internet Explorer. Safari before v10.1 and IE before v10 are not supported.

The mapshaper distribution includes the script `mapshaper-gui`, which runs mapshaper's web interface locally. You can also visit [mapshaper.org](http://www.mapshaper.org) to use mapshaper online.

All processing is done in the browser, so your data stays private, even when using the public website.

### Large file support

**Web interface**

Firefox is able to load Shapefiles and GeoJSON files larger than 1GB. Chrome has improved in recent versions, but is still prone to out-of-memory errors when importing files larger than several hundred megabytes.

**Command line interface**

When working with very large files, mapshaper may become unresponsive or crash with the message "JavaScript heap out of memory."

One option is to run `mapshaper-xl` (added in v0.4.63), which allocates more memory than the standard `mapshaper` program.

Another solution is to run Node directly with the `--max-old-space-size` option. The following example (Mac or Linux) allocates 8GB of memory:
```bash
$ node  --max-old-space-size=8192 `which mapshaper` <mapshaper commands>
```

### Installation

Mapshaper requires [Node.js](http://nodejs.org).

With Node installed, you can install the latest release version of mapshaper using npm. Install with the "-g" flag to make the executable scripts available systemwide.

```bash
npm install -g mapshaper
```

To install and run the latest development code from github:

```bash
git clone git@github.com:mbloch/mapshaper.git
cd mapshaper
npm install
bin/mapshaper     # run the command line program
bin/mapshaper-gui # use the web UI locally
```

### Building and testing

Run the `build` script to build both the cli and web UI modules.

Run `npm test` in the project directory to run mapshaper's tests.

### License

This software is licensed under [MPL 2.0](http://www.mozilla.org/MPL/2.0/).

According to Mozilla's [FAQ](http://www.mozilla.org/MPL/2.0/FAQ.html), "The MPL's ‘file-level’ copyleft is designed to encourage contributors to share modifications they make to your code, while still allowing them to combine your code with code under other licenses (open or proprietary) with minimal restrictions."



### Acknowledgements

My colleagues at The New York Times, for countless suggestions, bug reports and general helpfulness.

Mark Harrower, for collaborating on the original "MapShaper" program at the University of Wisconsin&ndash;Madison.

### 本地运行
进入mapshaper根路径37

**Web interface**

38



39

Firefox is able to load Shapefiles and GeoJSON files larger than 1GB. Chrome has improved in recent versions, but is still prone to out-of-memory errors when importing files larger than several hundred megabytes.

40



41

**Command line interface**

42



43

When working with very large files, mapshaper may become unresponsive or crash with the message "JavaScript heap out of memory."

44



45

One option is to run `mapshaper-xl` (added in v0.4.63), which allocates more memory than the standard `mapshaper` program.

46



47

Another solution is to run Node directly with the `--max-old-space-size` option. The following example (Mac or Linux) allocates 8GB of memory:

48

```bash

49

$ node  --max-old-space-size=8192 `which mapshaper` <mapshaper commands>

50

```

51



52

### Installation

53



54

Mapshaper requires [Node.js](http://nodejs.org).

55



56

With Node installed, you can install the latest release version of mapshaper using npm. Install with the "-g" flag to make the executable scripts available systemwide.

57



58

```bash

59

npm install -g mapshaper

60

```

61



62

To install and run the latest development code from github:

63



64

```bash

65

git clone git@github.com:mbloch/mapshaper.git

66

cd mapshaper

67

npm install

68

bin/mapshaper     # run the command line program

69

bin/mapshaper-gui # use the web UI locally

70

```

71



72

### Building and testing

73



74

Run the `build` script to build both the cli and web UI modules.

75



76

Run `npm test` in the project directory to run mapshaper's tests.

77



78

### License

79



80

This software is licensed under [MPL 2.0](http://www.mozilla.org/MPL/2.0/).

81



82

According to Mozilla's [FAQ](http://www.mozilla.org/MPL/2.0/FAQ.html), "The MPL's ‘file-level’ copyleft is designed to encourage contributors to share modifications they make to your code, while still allowing them to combine your code with code under other licenses (open or proprietary) with minimal restrictions."

83



84



85



86

### Acknowledgements

87



88

My colleagues at The New York Times, for countless suggestions, bug reports and general helpfulness.

89



90

Mark Harrower, for collaborating on the original "MapShaper" program at the University of Wisconsin&ndash;Madison.

91



92

### 本地运行

93

 进入mapshaper根路径
1. 安装依赖
执行：npm install
2. 编译：
执行： node build
3. 运行web服务：
执行： node bin/mapshaper-gui  
运行成功后会自动打开默认浏览器：http://localhost:5555/ 

