## Build
1. Install EMSDK following https://docs.opencv.org/3.4/d4/da1/tutorial_js_setup.html
2. Clone the modified [opencv](https://github.com/longcw/opencv) and [opencv_contrib](https://github.com/longcw/opencv_contrib)
   ```bash
   cd /path/to/work_dir
   git clone -b feat/wechat_qrcode_js https://github.com/longcw/opencv.git
   git clone -b feat/wechat_qrcode_js https://github.com/longcw/opencv_contrib.git
   ```
3. Build
   ```bash
   cd /path/to/work_dir
   emcmake python ./opencv/platforms/js/build_js.py build_js --build_test --cmake_option="-DOPENCV_EXTRA_MODULES_PATH=/path/to/work_dir/opencv_contrib/modules"
   ```
4. Download models from https://github.com/WeChatCV/opencv_3rdparty/

## Example
This repo includes a built opencv.js and a test script in [example](./example).
```bash
cd example
python -m http.server 8000
# Run the example in http://0.0.0.0:8000/test.html
```