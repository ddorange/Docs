# C++入門
cocos2d-xをはじめるために、C++の基本っぽいことをメモ  
  
参考
- http://www.asahi-net.or.jp/~yf8k-kbys/newcpp0.html

## 変数
`型　+ 変数名;`で宣言する
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
``` cpp
// クラスの定義 ----------------------------------
class Dog
{
// プライベート変数
private:
    string name;
    int age;

// パブリック変数
public:
    Dog(string);      // コンストラクタの定義
    void speak() const; // メソッドの定義
};

// クラスの中身 ----------------------------------
// コンストラクタの中身
Dog::Dog(string s) : name(s){}

// メソッドの中身
void Dog::speak() const{
    cout<<"私の名前は"<<name<<"です。"<<endl;
}

// 実行
int main(){
    // インスタンスを生成
    Dog dog_01("ポチ");

    // speakメソッドを実行
    dog_01.speak();
}
```
