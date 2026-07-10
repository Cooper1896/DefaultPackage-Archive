# Kongyingmap Overseas Update Workaround / 空荧酒馆更新修复

A temporary mirror and workaround for the Kongyingmap client getting stuck on the "updating manifest" screen for users outside Mainland China.

本仓库为海外直连无法更新空荧酒馆（卡在“更新清单/updating manifest”）的玩家提供临时文件镜像与修复方案。

---

## BACKUP FIRST!!! / 请先备份！

> ** Before proceeding, please make a backup of your original folder!** If anything goes wrong, you can easily restore it to avoid breaking the client.
> 
> ** 在进行任何操作之前，请务必先备份原文件夹！** 如果替换后出现任何问题，你可以随时还原，避免客户端彻底损坏。

---

## How to Use / 使用方法

The client reads `ManifestFiles` to figure out which hashed bundles it needs. By replacing the entire `DefaultPackage` folder, we can bypass the broken overseas CDN manifest check.
客户端需要读取 `ManifestFiles` 来识别它需要哪些哈希 Bundle 文件。通过整体替换 `DefaultPackage` 文件夹，我们可以直接跳过海外 CDN 报错的清单检查。

### Default Path / 默认路径
`C:\Program Files\KongYingMap\Map_Data\package\DefaultPackage`

### Steps / 操作步骤

#### Step 1: Backup / 第一步：备份原文件
* Go to `C:\Program Files\KongYingMap\Map_Data\package\DefaultPackage`
, copy your original `DefaultPackage` folder, and paste it somewhere (e.g., your Desktop) as a backup.
  前往上述路径，把原本的 `DefaultPackage` 文件夹复制一份保存到安全的地方（比如桌面）作为备份。

#### Step 2: Download from GitHub / 第二步：从 GitHub 下载
* Look at the top right of this repository page, click the green **`<> Code`** button.
  看向本仓库页面的右上角，点击绿色的 **`<> Code`** 按钮。
* In the dropdown menu, click **`Download ZIP`** to download the repository source code to your PC.
  在弹出的下拉菜单中，点击 **`Download ZIP`**，将本仓库的源码压缩包下载到电脑上。

#### Step 3: Unzip & Locate / 第三步：解压并找到文件夹
* Locate the downloaded `.zip` file, right-click it, and select **"Extract All..."** (or use 7-Zip / WinRAR) to unzip it.
  找到下载好的 `.zip` 压缩包，右键选择 **“全部解压...”**（或使用 7-Zip / WinRAR）将其解压。

#### Step 4: Replace & Launch / 第四步：替换并启动
* Copy and overwrite all the unzipped files into the path: `C:\Program Files\KongYingMap\Map_Data\package\DefaultPackage`
  将全部解压出来的文件覆盖到路径：`C:\Program Files\KongYingMap\Map_Data\package\DefaultPackage`
* Restart the Kongyingmap client. It should work now😊
  重新打开空荧酒馆客户端，此时应该会直接跳过更新检查并正常进入。
It should look like this,
C:\Program Files\KongYingMap\Map_Data\package\DefaultPackage
├─ CacheFiles 
├─ ManifestFiles 
├─ .gitattributes 
├─ ApplicationFootPrint.bytes 
└─ README.md (optional)
---

This is an unofficial community workaround.This repository will be archived once the official CDN issue is resolved.

本仓库仅为社区玩家临时救急使用。官方修复 CDN 后本仓库将会归档。
