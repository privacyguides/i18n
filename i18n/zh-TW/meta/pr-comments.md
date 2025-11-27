---
title: 對 PR 的討論
description: 參與 Pull Request 討論的指南。
---

在 GitHub PR 中留下註解或進行審核時，請避免使用一般的 **Add a comment** 方塊。

![請勿使用 GitHub 一般的 "Add a comment" 區塊](../assets/img/meta/pr-avoid-general-comments.png)

以這個方式留下的註解不會拆分成_討論串_，在有多個對話進行時很難追蹤。

以下列方式留下的註解則會有內建的回覆區塊，讓對話固定在同一個討論串中。 討論結束後，也可以標示為已解決，讓討論更容易追蹤。

![GitHub 內建「回覆」方塊的註解擷圖，以橘色強調。](../assets/img/meta/pr-threaded-comment.png)

## 註解

請將所有註解留在 PR 的 :octicons-file-diff-16: **Files changed** 標籤的下方以開始討論。

![Pull request 的標籤擷圖。 "Files changed" 標籤有深橘色外框。](https://docs.github.com/assets/cb-23571/mw-1440/images/help/pull_requests/pull-request-tabs-changed-files.webp)

若要對 PR 留下_一般性_的註解，請點擊檔案右方的 :octicons-comment-16: 評論圖示：

![Pull request 的 "Files changed" 頁面當中圖檔的擷圖。 檔案右側，註解圖示有橘色外框。](https://docs.github.com/assets/cb-73771/mw-1440/images/help/pull_requests/pull-request-comment-on-file.webp)

如果 PR 一次變更了多個檔案，則只註解主要或最相關的變更檔案；如果無法決定，則註解在第一個檔案。

若只要對 PR 的_特定行_留下註解，請將滑鼠停留在您要新增註解的那一行，然後點擊藍色的註解圖示：

![Pull request 當中的修改差異擷圖。 在行號旁邊，有一個橘色外框強調的藍色加號圖示。](https://docs.github.com/assets/cb-44227/mw-1440/images/help/commits/hover-comment-icon.webp)

（您也可以選擇性一次針對多行加入註解。 點擊想要加入註解的第一行，然後向下拖曳出要註解的範圍，再點擊範圍最後一行的藍色註解圖示。 或者也可以點擊要註解的第一行旁邊的藍色註解圖示，然後往下拖曳至要註解的最後一行。)

然後輸入註解，再點擊 **Add single comment**。

## 審核

進行審核時，請依照上述步驟，但點擊 **Start a review**（然後是 **Add a review comment**），而非 **Add single comment**。

然後點擊頁面頂端的 **Finish your review** 按鈕。

不要在完成審核的彈出視窗當中的 _Leave a comment_ 留下任何討論註解。 您可以留空，不需要後續任何處理的話也可以留下一段簡短說明。 若要對需要進一步討論的內容留下註解，則依照上面描述的方式進行。

然後按下 **Submit review**。
