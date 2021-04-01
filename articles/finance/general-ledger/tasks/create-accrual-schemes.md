---
title: สร้างแบบแผนการรับรู้
description: หัวข้อนี้อธิบายวิธีการสร้างแบบแผนการรับรู้
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccrualTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5c021f71735e63c270e8f1998d77d4e4abcc5506
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236709"
---
# <a name="create-accrual-schemes"></a><span data-ttu-id="a51fa-103">สร้างแบบแผนการรับรู้</span><span class="sxs-lookup"><span data-stu-id="a51fa-103">Create accrual schemes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a51fa-104">หัวข้อนี้อธิบายวิธีการสร้างแบบแผนการรับรู้</span><span class="sxs-lookup"><span data-stu-id="a51fa-104">This topic explains how to create an accrual scheme.</span></span> <span data-ttu-id="a51fa-105">งานนี้ใช้บริษัทสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="a51fa-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="a51fa-106">ไปที่ **บานหน้าต่างนำทาง > โมดูล > บัญชีแยกประเภททั่วไป > การตั้งค่าสมุดรายวัน > แบบแผนการรับรู้**</span><span class="sxs-lookup"><span data-stu-id="a51fa-106">Go to **Navigation pane > Modules > General ledger > Journal setup > Accrual schemes**.</span></span>
2. <span data-ttu-id="a51fa-107">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="a51fa-107">Select **New**.</span></span>
3. <span data-ttu-id="a51fa-108">ในฟิลด์ **การระบุรายการค้างรับค้างจ่าย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a51fa-108">In the **Accrual identification** field, type a value.</span></span>
4. <span data-ttu-id="a51fa-109">ในฟิลด์ **คำอธิบายเกี่ยวกับแผนการรับรู้** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a51fa-109">In the **Description of accrual scheme** field, type a value.</span></span>
5. <span data-ttu-id="a51fa-110">ในฟิลด์ **เดบิต** ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="a51fa-110">In the **Debit** field, specify the desired values.</span></span> <span data-ttu-id="a51fa-111">บัญชีหลักที่กำหนดไว้จะแทนเดบิตบัญชีหลักในบรรทัดสมุดรายวันใบสำคัญ และยังสามารถใช้สำหรับการกลับรายการยืดเวลาซึ่งขึ้นอยู่กับธุรกรรมการรับรู้บัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="a51fa-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="a51fa-112">ในฟิลด์ **เครดิต** ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="a51fa-112">In the **Credit** field, specify the desired values.</span></span> <span data-ttu-id="a51fa-113">บัญชีหลักที่กำหนดไว้จะแทนเครดิตบัญชีหลักในบรรทัดสมุดรายวันใบสำคัญ และยังจะสามารถใช้สำหรับการกลับรายการยืดเวลาขึ้นอยู่กับธุรกรรมการรับรู้บัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="a51fa-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="a51fa-114">ในฟิลด์ **ใบสำคัญ** ให้เลือกวิธีที่คุณต้องการกำหนดใบสำคัญ เมื่อลงรายการบัญชีธุรกรรมแล้ว</span><span class="sxs-lookup"><span data-stu-id="a51fa-114">In the **Voucher** field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="a51fa-115">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าเพื่ออธิบายธุรกรรมที่จะลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="a51fa-115">In the **Description** field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="a51fa-116">ในฟิลด์ **ความถี่ของรอบระยะเวลา** ให้เลือกความถี่ที่ธุรกรรมควรเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="a51fa-116">In the **Period frequency** field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="a51fa-117">ในฟิลด์ **จำนวนครั้งที่เกิดขึ้นตามรอบระยะเวลา** ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="a51fa-117">In the **Number of occurrences by period** field, enter a number.</span></span>
11. <span data-ttu-id="a51fa-118">ในฟิลด์ **ลงรายการบัญชีธุรกรรม** ให้เลือกเวลาที่ควรจะลงรายการบัญชีธุรกรรม เช่น **รายเดือน**</span><span class="sxs-lookup"><span data-stu-id="a51fa-118">In the **Post transactions** field, select when the transactions should be posted, such as **Monthly**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]