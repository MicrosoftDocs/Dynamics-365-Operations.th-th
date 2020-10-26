---
title: เปิดใช้งานการคำนวณภาษีที่ล่าช้าในสมุดรายวัน
description: หัวข้อนี้อธิบายวิธีการเปิดใช้งานคุณลักษณะการคำนวณภาษีที่ล่าช้าในสมุดรายวัน เพื่อช่วยปรับปรุงประสิทธิภาพการคำนวณภาษี เมื่อจำนวนรายการสมุดรายวันมีปริมาณมาก
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
ms.author: roschlom
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: d4ce0343ac766b30d532be0866a381dc520fd462
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977154"
---
# <a name="enable-delayed-tax-calculation-on-journals"></a><span data-ttu-id="db65c-103">เปิดใช้งานการคำนวณภาษีที่ล่าช้าในสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="db65c-103">Enable delayed tax calculation on journals</span></span>
[!include [banner](../includes/banner.md)]


<span data-ttu-id="db65c-104">หัวข้อนี้อธิบายวิธีการที่คุณสามารถทำให้การคำนวณภาษีขายล่าช้าลงในสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="db65c-104">This topic explains how you can delay sales tax calculation on journals.</span></span> <span data-ttu-id="db65c-105">ความสามารถนี้จะช่วยปรับปรุงประสิทธิภาพการทำงานของการคำนวณภาษีเมื่อมีรายการสมุดรายวันหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="db65c-105">This capability helps improve the performance of tax calculations when there are many journal lines.</span></span>

<span data-ttu-id="db65c-106">ตามค่าเริ่มต้น ยอดภาษีขายในรายการสมุดรายวันจะถูกคำนวณเมื่อใดก็ตามที่มีการอัพเดตฟิลด์ที่เกี่ยวข้องกับภาษี</span><span class="sxs-lookup"><span data-stu-id="db65c-106">By default, sales tax amounts on journal lines are calculated whenever tax-related fields are updated.</span></span> <span data-ttu-id="db65c-107">ฟิลด์เหล่านี้รวมไปถึงฟิลด์สำหรับกลุ่มภาษีขายและกลุ่มภาษีขายตามประเภทสินค้า</span><span class="sxs-lookup"><span data-stu-id="db65c-107">These fields include the fields for sales tax groups and item sales tax groups.</span></span> <span data-ttu-id="db65c-108">การอัพเดตใดๆ ที่เกิดขึ้นกับรายการสมุดรายวันจะทำให้มีการคำนวณจำนวนเงินภาษีใหม่สำหรับรายการสมุดรายวันทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="db65c-108">Any update to a journal line causes tax amounts to be recalculated for all journal lines.</span></span> <span data-ttu-id="db65c-109">ถึงแม้ว่าลักษณะการทำงานนี้จะช่วยให้ผู้ใช้เห็นยอดภาษีที่คำนวณได้ในเวลาจริง การทำงานนี้อาจส่งผลกระทบต่อประสิทธิภาพการทำงานได้หากจำนวนรายการสมุดรายวันมีจำนวนเยอะมาก</span><span class="sxs-lookup"><span data-stu-id="db65c-109">Although this behavior helps user see tax amounts calculated in real time, it can also affect performance if the number of journal lines is very large.</span></span>

<span data-ttu-id="db65c-110">คุณลักษณะการคำนวณภาษีที่ล่าช้า ช่วยให้คุณสามารถหน่วงเวลาการคำนวณภาษีในสมุดรายวัน ดังนั้นจึงช่วยแก้ไขปัญหาประสิทธิภาพการทำงาน</span><span class="sxs-lookup"><span data-stu-id="db65c-110">The Delayed tax calculation feature lets you delay tax calculation on journals and therefore helps fix performance issues.</span></span> <span data-ttu-id="db65c-111">เมื่อเปิดใช้งานลักษณะการทำงานนี้ จะมีการคำนวณจำนวนเงินภาษีเฉพาะเวลาที่ผู้ใช้คลิก **ภาษีขาย** หรือลงรายการบัญชีสมุดรายวันเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="db65c-111">When this feature is turned on, tax amounts are calculated only when a user selects **Sales Tax** or posts the journal.</span></span>

<span data-ttu-id="db65c-112">คุณสามารถหน่วงเวลาการคำนวณภาษีขายได้สามระดับต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="db65c-112">You can delay the calculation of sales taxes at three levels:</span></span>

- <span data-ttu-id="db65c-113">นิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="db65c-113">Legal entity</span></span>
- <span data-ttu-id="db65c-114">ชื่อสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="db65c-114">Journal name</span></span>
- <span data-ttu-id="db65c-115">ส่วนหัวของสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="db65c-115">Journal header</span></span>

<span data-ttu-id="db65c-116">ระบบจะให้ความสำคัญกับการตั้งค่าสำหรับหัวข้อของสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="db65c-116">The system gives priority to the setting for the journal header.</span></span> <span data-ttu-id="db65c-117">ตามค่าเริ่มต้น การตั้งค่านี้นำมาจากชื่อของสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="db65c-117">By default, this setting is taken from the journal name.</span></span> <span data-ttu-id="db65c-118">ตามค่าเริ่มต้น การตั้งค่าสำหรับชื่อสมุดรายวันจะมีการนำมาจากเพจ **พารามิเตอร์บัญชีแยกประเภททั่วไป** เมื่อมีการสร้างชื่อสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="db65c-118">By default, the setting for the journal name is taken from the setting on the **General ledger parameters** page when the journal name is created.</span></span> <span data-ttu-id="db65c-119">ส่วนต่อไปนี้อธิบายวิธีการเปิดใช้งานการคำนวณภาษีที่ล่าช้าสำหรับนิติบุคคล ชื่อสมุดรายวันและหัวข้อของสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="db65c-119">The following sections explain how to turn on delayed tax calculation for legal entities, journal names, and journal headers.</span></span>

## <a name="turn-on-delayed-tax-calculation-at-the-legal-entity-level"></a><span data-ttu-id="db65c-120">เปิดใช้งานการคำนวณภาษีที่ล่าช้าที่ระดับนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="db65c-120">Turn on delayed tax calculation at the legal entity level</span></span>

1. <span data-ttu-id="db65c-121">ไปที่ **บัญชีแยกประเภททั่วไปr \> การตั้งค่าบัญชีแยกประเภท \>พารามิเตอร์บัญชีแยกประเภททั่วไป**</span><span class="sxs-lookup"><span data-stu-id="db65c-121">Go to **General ledger \> Ledger setup \> General ledger parameters**.</span></span>
2. <span data-ttu-id="db65c-122">บนแท็บ **ภาษีขาย** บนแท็บด่วน **ทั่วไป** ตั้งค่าตัวเลือก **การคำนวณภาษีที่ล่าช้า** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="db65c-122">On the **Sales tax** tab, on the **General** FastTab, set the **Delayed tax calculation** option to **Yes**.</span></span>

![รูปภาพพารามิเตอร์บัญชีแยกประเภททั่วไป](media/delayed-tax-calculation-gl.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-name-level"></a><span data-ttu-id="db65c-124">เปิดใช้งานการคำนวณภาษีที่ล่าช้าที่ระดับชื่อสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="db65c-124">Turn on delayed tax calculation at the journal name level</span></span>

1. <span data-ttu-id="db65c-125">ไปที่ **บัญชีแยกประเภททั่วไป \> การตั้งค่าสมุดรายวัน \> ชื่อสมุดรายวัน**</span><span class="sxs-lookup"><span data-stu-id="db65c-125">Go to **General ledger \> Journal setup \> Journal names**.</span></span>
2. <span data-ttu-id="db65c-126">บนแท็บด่วน **ทั่วไป** ในส่วน **ภาษีขาย** ตั้งค่าตัวเลือก **การคำนวณภาษีที่ล่าช้า** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="db65c-126">On the **General** FastTab, in the **Sales tax** section, set the **Delayed tax calculation** option to **Yes**.</span></span>

![รูปภาพชื่อสมุดรายวัน](media/delayed-tax-calculation-journal-name.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-header-level"></a><span data-ttu-id="db65c-128">เปิดใช้งานการคำนวณภาษีที่ล่าช้าที่ระดับหัวข้อของสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="db65c-128">Turn on delayed tax calculation at the journal header level</span></span>

1. <span data-ttu-id="db65c-129">ไปที่ **บัญชีแยกประเภททั่วไป \> รายการสมุดรายวัน \> สมุดรายวันทั่วไป**</span><span class="sxs-lookup"><span data-stu-id="db65c-129">Go to **General ledger \> Journal entries \> General journals**.</span></span>
2. <span data-ttu-id="db65c-130">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="db65c-130">Select **New**.</span></span>
3. <span data-ttu-id="db65c-131">เลือกชื่อสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="db65c-131">Select a journal name.</span></span>
4. <span data-ttu-id="db65c-132">บนแท็บ **การตั้งค่า** ให้ตั้งค่าตัวเลือก **การคำนวณภาษีที่ล่าช้า** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="db65c-132">On the **Setup** tab, set the **Delayed tax calculation** option to **Yes**.</span></span>

![รูปภาพเพจสมุดรายวันทั่วไป](media/delayed-tax-calculation-journal-header.png)
