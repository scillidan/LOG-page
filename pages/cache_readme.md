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
- faster-whisper-webui
  collapsed:: true
	- ```sh
	  git clone https://github.com/Cerlancism/faster-whisper-webui
	  cd faster-whisper-webui
	  ```
	  
	  Edit `requirements-fasterWhisper.txt`:
	  
	  ```sh
	  torch==2.0.1
	  torchaudio==2.0.2
	  pyannote.audio==3.0.1
	  ```
	  
	  ```sh
	  python310 -m venv venv
	  venv\Scripts\activate.bat
	  pip install -r requirements-fasterWhisper.txt
	  pip install torch===2.0.1 torchaudio===2.0.2 pyannote.audio===3.0.1 -f https://download.pytorch.org/whl/torch_stable.html
	  ```
	  
	  ```sh
	  python cli.py --whisper_implementation faster-whisper --vad silero-vad --auto_parallel true --vad_parallel_devices 0 --model large-v2 --language Chinese --initial_prompt "以下是普通話的句子。" --diarization_num_speakers 1 --output_dir D:\home ^|
	  ```
	  
	  如果你要使用本地模型，使用这个仓库，并按说明配置。
	  
	  先试运行`cli.py`，将下载对应的模型。之后可以使用`app.py`
	  
	  ```json
	  {
	    "input_audio_max_duration": 600, // -1
	    "server_port": 7860, // 7830
	    "whisper_implementation": "whisper", //  "faster-whisper"
	    "default_model_name": "medium", // "large-v2"
	    "vad_parallel_devices": "", // "0"
	    "auto_parallel": false, // true
	    "output_dir": null, // "D:/home"
	    "language": null, // "Chinese"
	  }
	  ```
	  
	  ```sh
	  python app.py --initial_prompt "以下是普通話的句子。"
	  ```
- Jupyter
	- ```sh
	  pip install --user ipykernel
	  ipython kernel install
	  jupyter-lab
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