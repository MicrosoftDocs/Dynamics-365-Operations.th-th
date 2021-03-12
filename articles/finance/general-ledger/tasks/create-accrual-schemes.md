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
ms.openlocfilehash: 457be741dfd3b44cb963db37857d6a7bceecc14e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994676"
---
# <a name="create-accrual-schemes"></a><span data-ttu-id="fb998-103">สร้างแบบแผนการรับรู้</span><span class="sxs-lookup"><span data-stu-id="fb998-103">Create accrual schemes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fb998-104">หัวข้อนี้อธิบายวิธีการสร้างแบบแผนการรับรู้</span><span class="sxs-lookup"><span data-stu-id="fb998-104">This topic explains how to create an accrual scheme.</span></span> <span data-ttu-id="fb998-105">งานนี้ใช้บริษัทสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="fb998-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="fb998-106">ไปที่ **บานหน้าต่างนำทาง > โมดูล > บัญชีแยกประเภททั่วไป > การตั้งค่าสมุดรายวัน > แบบแผนการรับรู้**</span><span class="sxs-lookup"><span data-stu-id="fb998-106">Go to **Navigation pane > Modules > General ledger > Journal setup > Accrual schemes**.</span></span>
2. <span data-ttu-id="fb998-107">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="fb998-107">Select **New**.</span></span>
3. <span data-ttu-id="fb998-108">ในฟิลด์ **การระบุรายการค้างรับค้างจ่าย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="fb998-108">In the **Accrual identification** field, type a value.</span></span>
4. <span data-ttu-id="fb998-109">ในฟิลด์ **คำอธิบายเกี่ยวกับแผนการรับรู้** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="fb998-109">In the **Description of accrual scheme** field, type a value.</span></span>
5. <span data-ttu-id="fb998-110">ในฟิลด์ **เดบิต** ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="fb998-110">In the **Debit** field, specify the desired values.</span></span> <span data-ttu-id="fb998-111">บัญชีหลักที่กำหนดไว้จะแทนเดบิตบัญชีหลักในบรรทัดสมุดรายวันใบสำคัญ และยังสามารถใช้สำหรับการกลับรายการยืดเวลาซึ่งขึ้นอยู่กับธุรกรรมการรับรู้บัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="fb998-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="fb998-112">ในฟิลด์ **เครดิต** ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="fb998-112">In the **Credit** field, specify the desired values.</span></span> <span data-ttu-id="fb998-113">บัญชีหลักที่กำหนดไว้จะแทนเครดิตบัญชีหลักในบรรทัดสมุดรายวันใบสำคัญ และยังจะสามารถใช้สำหรับการกลับรายการยืดเวลาขึ้นอยู่กับธุรกรรมการรับรู้บัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="fb998-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="fb998-114">ในฟิลด์ **ใบสำคัญ** ให้เลือกวิธีที่คุณต้องการกำหนดใบสำคัญ เมื่อลงรายการบัญชีธุรกรรมแล้ว</span><span class="sxs-lookup"><span data-stu-id="fb998-114">In the **Voucher** field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="fb998-115">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าเพื่ออธิบายธุรกรรมที่จะลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="fb998-115">In the **Description** field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="fb998-116">ในฟิลด์ **ความถี่ของรอบระยะเวลา** ให้เลือกความถี่ที่ธุรกรรมควรเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="fb998-116">In the **Period frequency** field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="fb998-117">ในฟิลด์ **จำนวนครั้งที่เกิดขึ้นตามรอบระยะเวลา** ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="fb998-117">In the **Number of occurrences by period** field, enter a number.</span></span>
11. <span data-ttu-id="fb998-118">ในฟิลด์ **ลงรายการบัญชีธุรกรรม** ให้เลือกเวลาที่ควรจะลงรายการบัญชีธุรกรรม เช่น **รายเดือน**</span><span class="sxs-lookup"><span data-stu-id="fb998-118">In the **Post transactions** field, select when the transactions should be posted, such as **Monthly**.</span></span>

