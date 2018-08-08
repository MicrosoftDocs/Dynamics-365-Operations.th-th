---
title: "นำเข้าและรักษาธุรกรรมบัตรเครดิต"
description: "หัวข้อนี้อธิบายวิธีการนำเข้าและรักษาธุรกรรมบัตรเครดิตที่เกี่ยวข้องกับค่าใช้จ่าย คุณสามารถตั้งค่าธุรกรรมเหล่านี้เพื่อให้ถูกนำเข้าตามกำหนดการที่เกิดซ้ำโดยอัตโนมัติ หรือคุณสามารถนำเข้าด้วยตนเองตามที่จำเป็น"
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 9674cf495b7fdd40d8672580b9d10e9ebe626bb0
ms.contentlocale: th-th
ms.lasthandoff: 08/07/2018

---

# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="cd53e-104">นำเข้าและรักษาธุรกรรมบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="cd53e-104">Import and maintain credit card transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd53e-105">คุณสามารถตั้งค่าธุรกรรมบัตรเครดิตที่เกี่ยวข้องกับค่าใช้จ่ายเพื่อให้นำเข้าโดยอัตโนมัติตามกำหนดการที่เกิดซ้ำได้</span><span class="sxs-lookup"><span data-stu-id="cd53e-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="cd53e-106">อีกทางหนึ่งคือ คุณสามารถนำเข้าธุรกรรมด้วยตนเองตามที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="cd53e-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="cd53e-107">ธุรกรรมบัตรเครดิตจะถูกนำเข้าผ่านเอนทิตี้ข้อมูลธุรกรรมบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="cd53e-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="cd53e-108">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับเอนทิตี้ข้อมูล โปรดดู [เอนทิตี้ข้อมูล](../../dev-itpro/data-entities/data-entities.md)</span><span class="sxs-lookup"><span data-stu-id="cd53e-108">For more information about data entities, see [Data entities](../../dev-itpro/data-entities/data-entities.md).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="cd53e-109">นำเข้าธุรกรรมบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="cd53e-109">Import credit card transactions</span></span>

1. <span data-ttu-id="cd53e-110">ในหน้า **ธุรกรรมบัตรเครดิต** เลือก **นำเข้าธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="cd53e-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="cd53e-111">ถ้าคุณเปิดการจัดการข้อมูลเป็นครั้งแรก ระบบจะต้องปรับปรุงรายการของเอนทิตี้ข้อมูลก่อนที่คุณจะดำเนินต่อได้</span><span class="sxs-lookup"><span data-stu-id="cd53e-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="cd53e-112">ในฟิลด์ **ชื่อ** ให้ป้อนคำอธิบายเฉพาะสำหรับงานนำเข้า</span><span class="sxs-lookup"><span data-stu-id="cd53e-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="cd53e-113">ในฟิลด์ **รูปแบบข้อมูลต้นทาง** เลือกรูปแบบไฟล์ที่ประกอบด้วยธุรกรรมบัตรเครดิตที่จะนำเข้า</span><span class="sxs-lookup"><span data-stu-id="cd53e-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="cd53e-114">เลือก **อัพโหลด** แล้วค้นหาและเลือกไฟล์ที่จะนำเข้า</span><span class="sxs-lookup"><span data-stu-id="cd53e-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="cd53e-115">หลังจากที่อัพโหลดไฟล์แล้ว ให้ตรวจสอบการแม็ปของไฟล์ธุรกรรมบัตรเครดิตและคอลัมน์ของเอนทิตี้ข้อมูลธุรกรรมบัตรเครดิตโดยการเลือกลิงก์ **ดูแผนที่** บนไทล์</span><span class="sxs-lookup"><span data-stu-id="cd53e-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="cd53e-116">ถ้ามีข้อผิดพลาดในการแม็ป หรือถ้าคุณต้องเปลี่ยนการแม็ป ให้ทำการเปลี่ยนแปลงการแม็ปจากแท็บ **การแสดงภาพการแม็ป** หรือแท็บ **รายละเอียดของการแม็ป**</span><span class="sxs-lookup"><span data-stu-id="cd53e-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="cd53e-117">เมื่อต้องการทำธุรกรรมบัตรเครดิตโดยอัตโนมัติ เลือก **สร้างงานข้อมูลที่เกิดซ้ำ**</span><span class="sxs-lookup"><span data-stu-id="cd53e-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="cd53e-118">จากนั้นคุณสามารถตั้งค่าการเกิดซ้ำที่กำหนดความถี่ที่ควรนำเข้าธุรกรรมบัตรเครดิตได้</span><span class="sxs-lookup"><span data-stu-id="cd53e-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="cd53e-119">เมื่อคุณได้ทำเสร็จสิ้นแล้ว เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cd53e-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="cd53e-120">เมื่อต้องการนำเข้าไฟล์ที่เลือกทันที เลือก **นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="cd53e-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="cd53e-121">ถ้ามีข้อผิดพลาดเกิดขึ้นในระหว่างการนำเข้า คุณสามารถดูล็อกการดำเนินการหรือข้อมูลการจัดเตรียมเพื่อดูข้อผิดพลาดที่คุณต้องแก้ไขเพื่อช่วยรับประกันการนำเข้าที่สำเร็จ</span><span class="sxs-lookup"><span data-stu-id="cd53e-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="cd53e-122">ถ้าคุณต้องนำเข้ารูปแบบไฟล์มากกว่าหนึ่งรายการ คุณต้องสร้างงานนำเข้าที่แยกต่างหากสำหรับชนิดรูปแบบแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="cd53e-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="cd53e-123">กำหนดธุรกรรมบัตรเครดิตสำหรับพนักงานที่สิ้นสุดการจ้างงานใหม่</span><span class="sxs-lookup"><span data-stu-id="cd53e-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="cd53e-124">หลังจากที่เรกคอร์ดพนักงานสิ้นสุด บัญชี Active Directory Domain Services (AD DS) ของพนักงานจะถูกปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="cd53e-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="cd53e-125">อย่างไรก็ตาม อาจมีธุรกรรมบัตรเครดิตที่ใช้งานอยู่ที่ยังคงมีค่าใช้จ่ายและต้องชำระเงินคืน</span><span class="sxs-lookup"><span data-stu-id="cd53e-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="cd53e-126">จากหน้า **ธุรกรรมบัตรเครดิต** คุณสามารถกำหนดพนักงานสำหรับธุรกรรมบัตรเครดิตโดยพนักงานที่เกี่ยวข้องนั้นถูกเลิกจ้างพนักงานแล้วใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="cd53e-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="cd53e-127">เลือกธุรกรรมบัตรเครดิตอย่างน้อยหนึ่งรายการ และจากนั้น เลือก **กำหนดธุรกรรมใหม่**</span><span class="sxs-lookup"><span data-stu-id="cd53e-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="cd53e-128">คุณสามารถเลือกพนักงานคนอื่นเพื่อกำหนดธุรกรรมบัตรเครดิตให้</span><span class="sxs-lookup"><span data-stu-id="cd53e-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="cd53e-129">หลังจากที่คุณกำหนดธุรกรรมบัตรเครดิตใหม่แล้ว คุณสามารถเลือกรายการเหล่านั้นสำหรับรายงานค่าใช้จ่าย และทำการชำระผ่านกระบวนการปกติสำหรับการชำระเงินคืนตามรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="cd53e-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

