# C++入門
cocos2d-xをはじめるために、C++の基本っぽいことをメモ  
  
参考
- http://www.asahi-net.or.jp/~yf8k-kbys/newcpp0.html

## 変数
`型 + 変数名;`で宣言する
``` cpp
    int num;
    string name = "hoge";
```

## 基本的な型
型          | 説明
----------- | ---------------------
bool        | true / false
char        | 文字列
int         | 整数型
float       | 浮動小数点型
double      | 倍精度浮動小数点型
void        | 空データ

## クラス
### sample.h
``` cpp
class Dog
{
// プライベート変数
private:
    string name;

// パブリック変数
public:
    // コンストラクタ
    Dog(string);
    
    // デストラクタ
    ~Dog();
    
    // メソッド
    void speak() const;
};
```

### sample.cpp
``` cpp
// コンストラクタ
Dog::Dog(string s) : name(s)
{
  // body...
}

// デストラクタ
Dog::~Dog()
{
  // body...
}

// メソッドの中身
void Dog::speak() const
{
    cout<<"私の名前は"<<name<<"です。"<<endl;
}
```

### 実行とか
``` cpp
// インスタンスを生成
Dog dog_01("ポチ");

// speakメソッドを実行
dog_01.speak();
```
