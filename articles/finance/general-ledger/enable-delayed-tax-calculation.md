---
title: เปิดใช้งานการคำนวณภาษีที่ล่าช้าในสมุดรายวัน
description: หัวข้อนี้อธิบายวิธีการใช้ **เปิดใช้งานการคำนวณภาษีที่ล่าช้าในสมุดรายวัน** เพื่อปรับปรุงประสิทธิภาพการคำนวณภาษี เมื่อจำนวนบรรทัดสมุดรายวันมีปริมาณมาก
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 5a8ae30a007d3e2b8b7a9bc9eb7786f6e58246d0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180115"
---
# <a name="enable-delayed-tax-calculation-on-journal"></a><span data-ttu-id="e0d1c-103">เปิดใช้งานการคำนวณภาษีที่ล่าช้าในสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="e0d1c-103">Enable delayed tax calculation on journal</span></span>
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="e0d1c-104">หัวข้อนี้อธิบายวิธีการใช้ **เปิดใช้งานการคำนวณภาษีที่ล่าช้าในสมุดรายวัน** เพื่อปรับปรุงประสิทธิภาพการคำนวณภาษี เมื่อจำนวนบรรทัดสมุดรายวันมีปริมาณมาก</span><span class="sxs-lookup"><span data-stu-id="e0d1c-104">This topic explains how to use the **Enable delayed tax calculation on journal** feature to improve tax calculation performance when the volume of journal lines is huge.</span></span>

<span data-ttu-id="e0d1c-105">ลักษณะการทำงานการคำนวณภาษีขายปัจจุบันในสมุดรายวันเป็นแบบ real-time ซึ่งทริกเกอร์เมื่อผู้ใช้อัพเดตฟิลด์ที่เกี่ยวข้องกับภาษี เช่น กลุ่มภาษีขาย/กลุ่มภาษีขายตามประเภทสินค้า</span><span class="sxs-lookup"><span data-stu-id="e0d1c-105">Current sales tax calculation behavior on journal is real-time triggered when user updates tax related fields, e.g. sales tax group/item sales tax group.</span></span> <span data-ttu-id="e0d1c-106">การอัพเดตใด ๆ ในสมุดรายวัน จะคำนวณยอดภาษีใหม่ในสมุดรายวันทั้งหมดอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="e0d1c-106">Any update at journal line level will re-calculate tax amount on all journal lines.</span></span> <span data-ttu-id="e0d1c-107">จะช่วยให้ผู้ใช้สามารถดูยอดเงินภาษีที่คำนวณได้แบบเรียลไทม์ แต่อาจนำปัญหาด้านประสิทธิภาพไปใช้ถ้าจำนวนบรรทัดของสมุดรายวันมีปริมาณมาก</span><span class="sxs-lookup"><span data-stu-id="e0d1c-107">It helps user to see real-time calculated tax amount but it could also bring performance issue if  the volume of journal lines is huge.</span></span>

<span data-ttu-id="e0d1c-108">ลักษณะการทำงานนี้จะให้ตัวเลือกในการหน่วงเวลาการคำนวณภาษีเพื่อแก้ไขปัญหาประสิทธิภาพการทำงาน</span><span class="sxs-lookup"><span data-stu-id="e0d1c-108">This feature provides an option to delay tax calculation to solve performance issue.</span></span> <span data-ttu-id="e0d1c-109">ถ้าเปิดใช้งานลักษณะการทำงานนี้ จะมีการคำนวณจำนวนเงินภาษีเมื่อผู้ใช้คลิก "ภาษีขาย" เท่านั้นหรือลงรายการบัญชีสมุดรายวันเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="e0d1c-109">If this feature is turned on, tax amount will only be calculated when user clicks "Sales Tax" command or posts the journal.</span></span>

<span data-ttu-id="e0d1c-110">ผู้ใช้สามารถ เปิด/ปิด พารามิเตอร์นี้ได้สามระดับ:</span><span class="sxs-lookup"><span data-stu-id="e0d1c-110">User can turn on/off the parameter at three levels:</span></span>
- <span data-ttu-id="e0d1c-111">โดยนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="e0d1c-111">By legal entity</span></span>
- <span data-ttu-id="e0d1c-112">โดยชื่อสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="e0d1c-112">By journal name</span></span>
- <span data-ttu-id="e0d1c-113">โดยส่วนหัวของสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="e0d1c-113">By journal header</span></span>

<span data-ttu-id="e0d1c-114">ระบบจะใช้ค่าพารามิเตอร์ในส่วนหัวของสมุดรายวันเป็นขั้นสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="e0d1c-114">System will take the parameter value on journal header as final.</span></span> <span data-ttu-id="e0d1c-115">ค่าพารามิเตอร์ในส่วนหัวของสมุดรายวันจะเป็นค่าเริ่มต้นจากชื่อสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="e0d1c-115">Parameter value on journal header will be defaulted from journal name.</span></span> <span data-ttu-id="e0d1c-116">ค่าพารามิเตอร์ในชื่อสมุดรายวันจะเป็นค่าเริ่มต้นจากพารามิเตอร์บัญชีแยกประเภททั่วไป เมื่อมีการสร้างชื่อสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="e0d1c-116">Parameter value on journal name will be defaulted from general ledger parameter when the journal name is created.</span></span>

<span data-ttu-id="e0d1c-117">"ยอดภาษีขายจริง" และ "ยอดเงินภาษีขายที่คำนวณได้" ในสมุดรายวันจะถูกซ่อนไว้ ถ้ามีการเปิดใช้งานพารามิเตอร์นี้</span><span class="sxs-lookup"><span data-stu-id="e0d1c-117">"Actual sales tax amount" and "Calculated sales tax amount" fields on journal will be hided if this parameter is turned on.</span></span> <span data-ttu-id="e0d1c-118">วัตถุประสงค์เพื่อให้ผู้ใช้ไม่สับสน เนื่องจากค่าของฟิลด์สองฟิลด์เหล่านี้จะแสดง 0 เสมอก่อนที่ผู้ใช้จะทริกเกอร์การคำนวณภาษี</span><span class="sxs-lookup"><span data-stu-id="e0d1c-118">The purpose is not to confuse user because the value of these two fields will always show 0 before user trigger the tax calculation.</span></span>

## <a name="enable-delayed-tax-calculation-by-legal-entity"></a><span data-ttu-id="e0d1c-119">เปิดใช้งานการคำนวณภาษีที่ล่าช้าโดยเรียงตามนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="e0d1c-119">Enable delayed tax calculation by legal entity</span></span>

1. <span data-ttu-id="e0d1c-120">ไปที่ **บัญชีแยกประเภททั่วไป > การตั้งค่าบัญชีแยกประเภท > พารามิเตอร์บัญชีแยกประเภททั่วไป**</span><span class="sxs-lookup"><span data-stu-id="e0d1c-120">Go to **General ledger > Ledger setup > General ledger parameters**</span></span>
2. <span data-ttu-id="e0d1c-121">คลิกแท็บ **ภาษีขาย**</span><span class="sxs-lookup"><span data-stu-id="e0d1c-121">Click **Sales tax** tab</span></span>
3. <span data-ttu-id="e0d1c-122">ภายใต้แท็บด่วน **ทั่วไป** หาพารามิเตอร์ **การคำนวณภาษีที่ล่าช้า** ให้เปิด/ปิด</span><span class="sxs-lookup"><span data-stu-id="e0d1c-122">Under **General** fast tab, find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-gl.png)



## <a name="enable-delayed-tax-calculation-by-journal-name"></a><span data-ttu-id="e0d1c-123">เปิดใช้งานการคำนวณภาษีที่ล่าช้าตามชื่อสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="e0d1c-123">Enable delayed tax calculation by journal name</span></span>

1. <span data-ttu-id="e0d1c-124">ไปที่ **บัญชีแยกประเภททั่วไป > การตั้งค่าสมุดรายวัน > ชื่อสมุดรายวัน**</span><span class="sxs-lookup"><span data-stu-id="e0d1c-124">Go to **General ledger > Journal setup > Journal names**</span></span>
2. <span data-ttu-id="e0d1c-125">ภายใต้แท็บด่วน **ทั่วไป** หาพารามิเตอร์ **การคำนวณภาษีที่ล่าช้า** ให้เปิด/ปิด</span><span class="sxs-lookup"><span data-stu-id="e0d1c-125">Under **General** fast tab, find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-journal-name.png)

## <a name="enable-delayed-tax-calculation-by-journal"></a><span data-ttu-id="e0d1c-126">เปิดใช้งานการคำนวณภาษีที่ล่าช้า ตามสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="e0d1c-126">Enable delayed tax calculation by journal</span></span>

1. <span data-ttu-id="e0d1c-127">ไปที่ **บัญชีแยกประเภททั่วไป > รายการสมุดรายวัน > สมุดรายวันทั่วไป**</span><span class="sxs-lookup"><span data-stu-id="e0d1c-127">Go to **General ledger > Journal entries > General journals**</span></span>
2. <span data-ttu-id="e0d1c-128">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="e0d1c-128">Click **New**</span></span>
3. <span data-ttu-id="e0d1c-129">เลือกชื่อสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="e0d1c-129">Select a journal name</span></span>
4. <span data-ttu-id="e0d1c-130">คลิก **ตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="e0d1c-130">Click **Setup**</span></span>
5. <span data-ttu-id="e0d1c-131">หาพารามิเตอร์ **การคำนวณภาษีที่ล่าช้า** ให้เปิด/ปิด</span><span class="sxs-lookup"><span data-stu-id="e0d1c-131">Find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-journal-header.png)
