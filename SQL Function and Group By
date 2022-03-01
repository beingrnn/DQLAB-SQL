USE dqlab;

## Fungsi Skalar Matematika - ABS() *mendapatkan nilai absolut*
SELECT
    studentid,
    firstname,
    lastname,
    semester1,
    semester2,
    ABS(markgrowth) AS markgrowth
FROM
    students;

## Fungsi Skalar Matematika - CEILING() *menampilkan nilai integer tebesar terdekat dari angka input*
SELECT
    studentid,
    firstname,
    lastname,
    CEILING(semester1) AS semester1,
    CEILING(semester2) AS semester2,
    markgrowth
FROM
    students;

## Fungsi Skalar Matematika - FLOOR() *menampilkan nilai integer terkecil terdekat dari angka input*
SELECT
    studentid,
    firstname,
    lastname,
    FLOOR(semester1) AS semester1,
    FLOOR(semester2) AS semester2,
    markgrowth
FROM
    students;

## Fungsi Skalar Matematika - ROUND() *nilai pembulatan 2 angka belakang koma*
SELECT
    studentid,
    firstname,
    lastname,
    ROUND(semester1, 1) AS semester1,
    ROUND(semester1, 0) AS semester2,
    markgrowth
FROM
    students;

## Fungsi Skalar Matematika - SQRT() *nilai kuadrat*
SELECT
    studentid,
    firstname,
    lastname,
    SQRT(semester1) AS semester1,
    semester2,
    markgrowth
FROM
    students;

## Fungsi Skalar Matematika *MOD = nilai sisa hasil pembagian, EXP = nilai ekponensial*
SELECT
    studentid,
    firstname,
    lastname,
    MOD(semester1, 2) AS semester1,
    semester2,
    EXP(markgrowth)
FROM
    students;

## Fungsi Text - CONCAT() *Menggabungkan kolom*
SELECT
    studentid,
    CONCAT(firstname, lastname) AS name,
    semester1,
    semester2,
    markgrowth
FROM
    students;

## Fungsi Text - SUBSTRING_INDEX() *untuk memisahkan teks (kolom, delimiter, index)*
SELECT
    studentid,
    substring_index(Email, '@', 1) AS name
FROM
    students;

## Fungsi Text - SUBSTR() *Extract nama (columnName, Start Index, Number of string to be extract)*
SELECT
    studentid,
    substr(firstname, 2, 3) AS initial
FROM
    students;

## Fungsi Text - LENGTH() *jumlah huruf*
SELECT
    studentid,
    firstname,
    LENGTH(firstname) AS total_char
FROM
    students;

## Fungsi Text - REPLACE() *mengubah isi kolom (ColumnName, Character/String to be change, New String/Character)*
SELECT
    studentid,
    email,
    REPLACE(email, 'yahoo', 'gmail') AS new_email
FROM
    students;

## Fungsi Text *UPPER/LOWER = mengubah menjadi huruf caps/kecil*
SELECT
    studentid,
    UPPER(firstname) AS firstname,
    LOWER(lastname) AS lastname
FROM
    students;

## Fungsi Aggregate - SUM() *menampilkan jumlah nilai dari kolom*
SELECT
    SUM(semester1) AS total_1,
    SUM(semester2) AS total_2
FROM
    students;

## Fungsi Aggregate - COUNT() *menampilkan jumlah kolom*
SELECT
    COUNT(firstname) AS total_student
FROM
    students;

## Fungsi Aggregate - AVG() *rata-rata nilai dalam kolom*
SELECT
    AVG(semester1) AS avg_1,
    AVG(semester2) AS avg_2
FROM
    students;

## Fungsi Aggregate *MIN/MAX = menampilkan nilai min dan max dalam kolom*

SELECT
    MIN(semester1) AS min1,
    MAX(semester1) AS max1,
    MIN(semester2) AS min2,
    MAX(semester2) AS max2
FROM
    students;

## Group by Single Column
SELECT
    province,
    COUNT(DISTINCT order_id) AS total_order,
    SUM(item_price) AS total_price
FROM
    sales_retail_2019
GROUP BY
    province;

## Group by Multiple Column
SELECT
    province,
    brand,
    COUNT(DISTINCT order_id) AS total_order,
    SUM(item_price) AS total_price
FROM
    sales_retail_2019
GROUP BY
    province,
    brand;

## Fungsi Aggregate dengan Grouping
SELECT
    province,
    COUNT(DISTINCT order_id) AS total_unique_order,
    SUM(item_price) AS revenue
FROM
    sales_retail_2019
GROUP BY
    province;

## Group By
SELECT
    MONTH(order_date) AS order_month,
    SUM(item_price) AS total_price,
    CASE
        WHEN sum(item_price) >= 30000000000 THEN 'Target Achieved'
        WHEN sum(item_price) <= 25000000000 THEN 'Less performed'
        ELSE 'Follow Up'
    END AS remark
FROM
    sales_retail_2019
GROUP BY
    MONTH(order_date);
