- Archivebox
	- ```sh
	  archivebox manage createsuperuser
	  archivebox server 127.0.0.1:8010
	  ```
- audiobookshelf
	- ```sh
	  fnm install 16.20.0
	  fnm use 16.20.0
	  ```
	  
	  ```sh
	  set NODE_ENV=production
	  npm i
	  npm install sequelize sequelize-cli --save
	  cd clinet
	  npm i
	  npm update vue
	  npm update fork-ts-checker-webpack-plugin
	  npm run generate
	  cd ..
	  ```
	  
	  Edit client/nuxt.config.js:
	  
	  ```
	  module.exports = {
	  ...
	  server: {
	    ...
	    host: '127.0.0.1'
	  },
	  ```
	  
	  ```sh
	  npm start
	  ```
	  
	  At same time:
	  
	  ```sh
	  cd client
	  npm start
	  ```
- av1an
  collapsed:: true
	- ```sh
	  scoop install vapoursynth vmaf
	  py .../vsrepo.py update
	  py .../vsrepo.py install lsmas ffms2
	  scoop install nasm emscripten
	  emsdk install latest
	  emsdk activate latest
	  ```
	  
	  ```sh
	  git clone https://github.com/m-ab-s/aom
	  mkdir aom-windows-build
	  cmake -S ./aom -B ./aom-windows-build -G "Visual Studio 17 2022"
	  cd ./aom-windows-build
	  cmake --build .
	  ```
- Jupyter
  collapsed:: true
	- ```sh
	  pip install --user ipykernel
	  ipython kernel install
	  jupyter-lab
	  ```
- Keyprinha
	- tldr
		- ```sh
		  scoop install tldr
		  tldr -c
		  ```
		  
		  Create symbolic link from `C:\Users\yourname\AppData\Roaming\tldr\pages.en` to `C:\Users\yourname\.cache\tldr\pages.en`
	- PuzzTools
		- ```sh
		  7z a PuzzTools.zip ./* -x!.git/ && mv PuzzTools.zip ...C:/Users/yourname/scoop/persist/keypirinha/portable/Profile/InstalledPackages/PuzzTools.keypirinha-package
		  ```
- komga
	- ```sh
	  for /d %%X in (*) do arenc.exe -e "v01.aren" -t folders -p . -m rename
	  for /d %%X in (*) do arenc.exe -e "001.aren" -t files -p %%X -m rename
	  for /d %%X in (*) do cp %%X/001.jpg %%X/cover.jpg
	  for /d %%X in (*) do py39 to_cbz.py %%X
	  python39 komga_cover_extractor.py -c "True" -cq "70" -p .
	  ```
- lobe-chat
	- ```sh
	  git clone https://github.com/lobehub/lobe-chat
	  cd lobe-chat
	  npm install
	  npm run build
	  ```
	  
	  edit `package.json`:
	  
	  ```json
	    "scripts": {
	  	...
	      "start": "next start -p 7850",
	      ...
	    },
	  ```
	  
	  ```sh
	  npm run start
	  ```
	-
- raphael-impress