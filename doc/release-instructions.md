# Releaseの作成

## 前提
- GitHub CLIが必要

## 手順
まず、タグ付けの対象となるコミットがリモートに存在する状態にしておく。

```
git push
```

以下のコマンドにて、新たにReleaseとして作成するタグ名を指定して、draftを作成する。

```
gh release create --generate-notes --draft --notes-start-tag test/v<prev> test/vX.Y.Z
gh release create --generate-notes --draft --notes-start-tag nuget/v<prev> nuget/vX.Y.Z
gh release create --generate-notes --draft --notes-start-tag release-target/v<prev> release-target/vX.Y.Z
gh release create --generate-notes --draft --notes-start-tag release-note/v<prev> release-note/vX.Y.Z
gh release create --generate-notes --draft --notes-start-tag actions/prepare-dotnet-sdk/v<prev> actions/prepare-dotnet-sdk/vX.Y.Z
```

以下のようにdraftを編集するためのURLが提示されるので、開く。

```
https://github.com/smdn/workflows-dotnet/releases/tag/untagged-XXXXXXXXXXXXXXXXXXXX
```

内容を検証・追記して問題なければ、[Publish Release]によってReleaseを公開にする。
