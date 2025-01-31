# Web 向けの Siv3D プログラミングを始める
Web ブラウザで動作する Siv3D が非公式で提供されています。Web 版にはいくつか制約や注意点があるため、Siv3D の使用に慣れた中級者以上を対象としています。利用にあたって困ったことがあれば Siv3D Discord サーバの `#web` チャンネルで質問してください。

## 利用ガイド
- [OpenSiv3D for Web :material-open-in-new:](https://siv3d.kamenokosoft.com/docs/ja/){:target="_blank"} を参照してください。
- 初回のビルドではエラーメッセージが表示されることがありますが、もう一度ビルドすると正常にビルドできます。
- Web 版のビルドでは、デフォルトで `engine/` と `example/` のすべてのファイルを最終出力に同梱するため、最終出力ファイルのサイズは Release ビルドでも合計数十 MB と大きくなります。そうしたアプリケーションを Web で公開すると、アクセスした利用者がファイルのダウンロードに時間がかかってしまうため、実際にアプリケーションを公開する際は、不要なファイルを削除する必要があります（参考: [チュートリアル 60. アプリの公開](../tutorial3/release.md)）。
- Emscripten リンカの設定において「追加の依存ファイル」からプログラムが使用していないライブラリ（例: `Siv3DScript`, `opencv_objdetect`, `opencv_photo`, `opencv_imgproc`, `turbojpeg`, `gif`, `webp`, `opusfile`, `opus`, `tiff`）を削除することで、Web 版の出力ファイルのサイズは、**最小で数 MB 程度** までコンパクトにできます。詳しくは Siv3D Discord サーバの `#web` チャンネルでご相談ください。
