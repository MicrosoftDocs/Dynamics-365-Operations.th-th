---
title: บันทึกหมายเลขใบรับรองการยินยอม TDS
description: หัวข้อนี้อธิบายวิธีการบันทึกหมายเลขใบรับรองการยินยอมหักภาษี ณ ที่จ่าย (TDS) ซึ่งออกให้แก่ผู้จัดจำหน่าย
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: f543adc8bab5ca224bdb672d6b3c282c2d8531d8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023616"
---
# <a name="record-tds-concession-certificate-numbers"></a><span data-ttu-id="2301b-103">บันทึกหมายเลขใบรับรองการยินยอม TDS</span><span class="sxs-lookup"><span data-stu-id="2301b-103">Record TDS concession certificate numbers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2301b-104">หัวข้อนี้อธิบายวิธีการบันทึกหมายเลขใบรับรองการยินยอมหักภาษี ณ ที่จ่าย (TDS) ซึ่งออกให้แก่ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2301b-104">This topic explains how to record the Tax Deducted at Source (TDS) concession certificate numbers that are issued to vendors.</span></span>

1. <span data-ttu-id="2301b-105">ไปที่ **ภาษี \> ภาษีทางอ้อม \> ภาษีหัก ณ ที่จ่าย \> การยินยอมภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="2301b-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax concessions**.</span></span>
2. <span data-ttu-id="2301b-106">ในฟิลด์ **ชนิดภาษี** ให้เลือก **TDS** เพื่อบันทึกใบรับรองการยินยอมของชนิดภาษี TDS</span><span class="sxs-lookup"><span data-stu-id="2301b-106">In the **Tax type** field, select **TDS** to record concession certificates for the TDS tax type.</span></span>
3. <span data-ttu-id="2301b-107">บนแท็บ **ภาพรวม** ให้เลือก **Alt+N** เพื่อสร้างบรรทัด</span><span class="sxs-lookup"><span data-stu-id="2301b-107">On the **Overview** tab, select **Alt+N** to create a line.</span></span>

    <span data-ttu-id="2301b-108">[![ส่วนหัวของรายการใหม่](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)</span><span class="sxs-lookup"><span data-stu-id="2301b-108">[![Header of the new line](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)</span></span>

4. <span data-ttu-id="2301b-109">ในฟิลด์ **รหัสภาษีหัก ณ ที่จ่าย** ให้เลือกรหัสภาษี TDS ที่จะออกใบรับรองการยินยอมให้แก่ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2301b-109">In the **Withholding tax code** field, select the TDS tax code that the vendor concession certificates are issued for.</span></span> <span data-ttu-id="2301b-110">ฟิลด์ **ชื่อรหัสภาษีหัก ณ ที่จ่าย** แสดงชื่อของรหัสภาษี TDS</span><span class="sxs-lookup"><span data-stu-id="2301b-110">The **Withholding tax code name** field shows the name of the TDS tax code.</span></span>
5. <span data-ttu-id="2301b-111">ในฟิลด์ **วันที่เริ่มต้น** และ **วันที่สิ้นสุด** ให้กําหนดรอบระยะเวลาที่มีผลบังคับใช้ให้กับใบรับรองการยินยอมที่ใช้รหัสภาษี TDS เพื่อคํานวณ TDS ให้กับผู้จัดจำหน่ายตามเกณฑ์การยินยอม</span><span class="sxs-lookup"><span data-stu-id="2301b-111">In the **From date** and **To date** fields, define the period of validity for the concession certificate that uses the TDS tax code to calculate TDS for the vendor on a concessional basis.</span></span>
6. <span data-ttu-id="2301b-112">ในฟิลด์ **หมายเหตุ** ให้ป้อนหมายเหตุใดๆ</span><span class="sxs-lookup"><span data-stu-id="2301b-112">In the **Remarks** field, enter any remarks.</span></span>
7. <span data-ttu-id="2301b-113">ในฟิลด์ **ส่วน** ป้อนรหัสตามกฎหมายที่ใบรับรองการยินยอม TDS ใช้ได้</span><span class="sxs-lookup"><span data-stu-id="2301b-113">In the **Section** field, enter the legal section code that the TDS concession certificate is availed under.</span></span>

    <span data-ttu-id="2301b-114">ถ้ารหัสส่วนคือ 197 ค่า "A" จะปรากฏขึ้นในทั้งคอลัมน์ "เหตุผลในการหัก/การลดหย่อน" ในแบบฟอร์ม 26Q และคอลัมน์ "เหตุผลในการไม่หัก/การหักลด/การเพิ่ม(ถ้ามี)" ในแบบฟอร์ม 27Q</span><span class="sxs-lookup"><span data-stu-id="2301b-114">If the section code is 197, the value "A" appears in both the "Reason for non-deduction/lower deduction" column in Form 26Q and the "Reason for non-deduction/lower deduction/grossing up (if any)" column in Form 27Q.</span></span> <span data-ttu-id="2301b-115">ถ้ารหัสส่วนคือ 197A ค่า "B" จะปรากฏขึ้นในทั้งสองคอลัมน์ดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="2301b-115">If the section code is 197A, the value "B" appears in both those places.</span></span>

8. <span data-ttu-id="2301b-116">เลือกแท็บต่วน **ใบรับรอง** เพื่อบันทึกหมายเลขใบรับรองการยินยอม TDS ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2301b-116">Select the **Certificate** FastTab to record TDS concession certificate numbers for vendors.</span></span>
9. <span data-ttu-id="2301b-117">ในฟิลด์ **บัญชีผู้จัดจำหน่าย** ให้เลือกบัญชีผู้จัดจำหน่าย ที่จะออกใบรับรองการยินยอม TDS</span><span class="sxs-lookup"><span data-stu-id="2301b-117">In the **Vendor account** field, select the vendor account that the TDS concession certificate is issued for.</span></span>
10. <span data-ttu-id="2301b-118">ในฟิลด์ **วันที่เริ่มต้น** และ **วันที่สิ้นสุด** ให้กําหนดรอบระยะเวลาการมีผลบังคับใช้ของใบรับรองการยินยอม TDS</span><span class="sxs-lookup"><span data-stu-id="2301b-118">In the **From date** and **To date** fields, define the period of validity for the TDS concession certificate.</span></span>

    <span data-ttu-id="2301b-119">การคํานวณ TDS ตามเกณฑ์การยินยอม จะยึดตามรอบระยะเวลาเมื่อมีการสร้างใบรับรองให้กับผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2301b-119">The calculation of TDS on a concessional basis is based on the period when the certificate is created for the vendor.</span></span>

11. <span data-ttu-id="2301b-120">ในฟิลด์ **ใบรับรอง** ป้อนหมายเลขใบรับรองการยินยอม TDS</span><span class="sxs-lookup"><span data-stu-id="2301b-120">In the **Certificate** field, enter the TDS concession certificate number.</span></span>

    <span data-ttu-id="2301b-121">[![แท็บด่วนใบรับรอง](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)</span><span class="sxs-lookup"><span data-stu-id="2301b-121">[![Certificate FastTab](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)</span></span>

12. <span data-ttu-id="2301b-122">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2301b-122">Close the page.</span></span>
