在 MSSQL 中，OBJECT_ID() 函數用於返回指定對象的物件識別碼（Object ID）。這個函數可以接受一個對象名稱作為參數，並返回該對象的唯一識別碼。
例如，如果你想要獲取一個表格的物件識別碼，你可以使用以下語法：
SELECT OBJECT_ID('TableName') AS ObjectID;

這將返回指定表格的物件識別碼。你可以將 'TableName' 替換為你想要查詢的實際表格名稱。
這個函數在某些情況下很有用，例如當你需要動態地查詢或操作不同的資料庫對象時，可以使用 OBJECT_ID() 函數來獲取對象的識別碼，以便進一步處理。

IF OBJECT_ID('TableName', 'U') IS NOT NULL
    PRINT '表格存在'
ELSE
    PRINT '表格不存在'
