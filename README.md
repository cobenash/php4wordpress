# PHP4Wordpress

[![Build Status](https://drone-v2.hellosanta.tw/api/badges/docker/php4wordpress/status.svg)](https://drone-v2.hellosanta.tw/docker/php4wordpress)

## 簡介
主要是根據php4drupal，概念製作一個可以給wordpress使用的php環境

## 主要功能
1. Tag來區分版本:
這個影像檔會根據Tag來區分不同的環境

2. SSH支援
由於開發的需要或某一些特殊的需求，我們會需要連進入容器進行處理，因此這個影像檔有提供SSH的支援，只需要將Public key當作參數丟進來，就可以使用Private Key連到容器內。

3. 調整Apache的環境
由於每個容器可能會需要調整上傳檔案大小、記憶體、Max_input_vars等重要的變數，因此這個部分將可以直接寫在environment的變數中，直接做調整。

4. 調整Web根目錄
可以根據個人需求調整網頁的根目錄，如果沒有設定根目錄，則這裡的會預設到 /var/www/html

5. Composer支援
由於在D8上面需要composer來執行眾多的指令並且更新很多元件，因此，這裡預設安裝composer進來

6. Healthy Check支援
已經原生將Healthy Check加入影像檔之中，可以通過status看到容器的狀態

## 支援環境變數
1. SSH_KEY
2. UPLOAD_MAX_FILESIZE
3. POST_MAX_SIZE
4. MEMORY_LIMIT
5. MAX_INPUT_VARS

## Docker-Compose使用方法
如果你想要用的是docker-compose的方法來使用這個Image的話，可以參考下面的範例

