# Releaseの作成

## 前提
- GitHub CLIが必要

## 手順
以下のコマンドにて、新たにReleaseとして作成するタグ名を指定して、draftを作成する。

```
gh release create --generate-notes --draft test/vX.Y.Z
gh release create --generate-notes --draft nuget/vX.Y.Z
gh release create --generate-notes --draft release-target/vX.Y.Z
```

以下のようにdraftを編集するためのURLが提示されるので、開く。

```
https://github.com/smdn/workflows-dotnet/releases/tag/untagged-XXXXXXXXXXXXXXXXXXXX
```

内容を検証・追記して問題なければ、[Publish Release]によってReleaseを公開にする。
