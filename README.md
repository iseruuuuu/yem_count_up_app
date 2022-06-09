# yem_count_up_app

# 作成の流れ

１、`cargo install wasm-pack`    
２、`cargo new --lib yew-app && cd yew-app`    
３、`lib.rs`に記載する    
４、`index.html`に記載する  
５、cargoのツールを使用してサーバを立ち上げる[`wasm-pack build --target web --out-name wasm --out-dir ./static`]  
６、Rust ツールチェイン(初回時のみ？？)[`curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh`]  
7、`rustup toolchain install nightly --allow-downgrade`を打ち込む（何のコマンドかわからない）    
8、 `rustup toolchain install stable-x86_64-unknown-linux-gnu --allow-downgrade`（何のコマンドかわからない）    
9、`cargo +nightly install miniserve`  
10、`miniserve ./static --index index.html`  


11,`http://127.0.0.1:8080/` or `http://localhost:8080/`を開く  

## Yewとは
→YewとはWebAssemblyを使用したマルチスレッドのUIフレームワーク(Reactのようなイメージ)  
→Webフロントフレームワーク  

### 特徴
・WebAssemblyに変換されるためブラウザ上での実行が可能  
・コンポーネントベースのフレームワークでReactやElmにかなり似ている(？)  
・JSとの互換性があるためNPMパッケージを使用して既存のJSアプリと統合可能(?)    
・DOM APIの呼び出しを最小にすることと、Webワーカーを使用して処理をバッググランドに簡単にオフロードすることで優れたパフォーマンスを出す    



## WebAssemblyとは
->C言語などの高級言語をブラウザ上で実行可能なバイナリ形式にする技術    
->直接WASMをさわることはなく、C言語やRustなどでコードを実装し、それらがWASMバイトコードにコンパイルされます。    
->コンパイルされたコードはWeb上で実行され、ネイティブマシンコードに変換されるため高速で動く、といった感じ    



# 参考サイト

https://ozway.jp/2020/10/rustwebassemblyyew%E3%81%A7todo%E3%82%A2%E3%83%97%E3%83%AA%E3%82%92%E5%AE%9F%E8%A3%85/

https://yew.rs/ja/docs/0.18.0/getting-started/build-a-sample-app

https://qiita.com/suzuki_sh/items/c53a6056bb4377a50861

https://blog.tagbangers.co.jp/ja/2020/06/07/getting-started-rust