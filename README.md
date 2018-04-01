## Angular JIT vs AOT 

Chrome timeline performance
![](https://habrastorage.org/webt/ov/1y/5m/ov1y5mfimskkisme7kewdrailmy.jpeg)

### Angular 2
```bash
cd angular2
npm install

# JIT Compilation
npm run build:prod
cd dist && httpserver

# AOT Compilation
npm run build:aot:prod
cd dist && httpserver
```

### Angular 4
```bash
cd angular4
npm install

# JIT Compilation
npm run build:prod
cd dist && httpserver

# AOT Compilation
npm run build:aot:prod
cd dist && httpserver
```

Go to: localhost:8000, open Chrome Dev Tools on the perfomance tab, and run the page several times to see the average download results

### Angular 5+

Usage AOT `ng build --aot --prod` or JIT `ng build --no-aot --prod --build-optimizer false`

### Note
* In the version of Angular 2, the assembly drops, however, the files are successfully compiled, after which you can start the local web server (the problem was solved in Angular 4)
