# kuokuo

##網站介紹

沒啥咪咚咚 ლ(•ω •ლ)

## 成品展示
[網站網址(host by heroku)](https://kuouko.herokuapp.com/)
![](https://github.com/lingyukuo/kuokuo/blob/master/screenshot.png)

## 使用方法
工具名稱 | 用途
---------|----------
Python 3 | 不需要解釋
Flask(python)    | 幫助我建立伺服器
HTML/CSS  | 網頁表示和排版
Heroku   | 託管網頁
Github   | 存放原始碼
Bootstrap | 顏色圖片模板
Markdown | 區段元素(網頁圖片)

## 程式碼片段
```python
@app.route("/")
def home():
    temp = glob.glob("articles/*")
    fill = []
    for t in temp:
        length = len(glob.glob(t + "/*.txt"))
        category = t.replace("articles/", "")
        f = (category, length)
        fill.append(f)
    return render_template("index.html", cat=fill)

```
