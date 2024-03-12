# Simple-LaTeX-OCR
The encoder is resnetv2+simplevit, the decoder is transformer, the attention mechanism uses flashattention2.0 from pytorch2.0, and the dataset size is 112 million

## Online experience

### https://huggingface.co/spaces/chaodreaming/Simple-LaTeX-OCR

### https://www.modelscope.cn/studios/chaodreaming/Simple-LaTeX-OCR/summary
Install the package `simple_latex_ocr`: 

```
pip install simple_latex_ocr
```

Use from within Python

    
    from simple_latex_ocr.models import Latex_OCR
    model = Latex_OCR()
    img_path = "tests/test_files/5.png"
    result = model.predict(img_path)
    print(result['formula'])
    print(result['confidence'])
    print(result['elapse'])

#### Used by command line
```bash
$ simple_latex_ocr tests/test_files/2.png


```


#### Used by api
```bash
$ python -m simple_latex_ocr.api.run

#You can use test.py to initiate a request for verification
```
## Contribution
Contributions of any kind are welcome.

## Acknowledgment
Code taken and modified from [lukas-blecher](https://github.com/lukas-blecher/LaTeX-OCR), [RapidAI](https://github.com/RapidAI/RapidLaTeXOCR),[ultralytics](https://github.com/ultralytics/ultralytics)
