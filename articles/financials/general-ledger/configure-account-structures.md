---
title: ตั้งค่าคอนฟิกโครงสร้างทางบัญชี
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับโครงสร้างทางบัญชีและมิติทางการเงิน
author: aprilolson
manager: AnnBe
ms.date: 05/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a0665f5aec2a0809ecb383c1d4adf4c2072c9569
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552036"
---
# <a name="configure-account-structures"></a><span data-ttu-id="40d9a-103">ตั้งค่าคอนฟิกโครงสร้างทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="40d9a-103">Configure account structures</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="40d9a-104">โครงสร้างทางบัญชีใช้บัญชีหลักและมิติทางการเงิน เพื่อสร้างชุดของกฎที่กำหนดใบสั่งและค่าที่ใช้เมื่อป้อนหมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="40d9a-104">Account structures use the main account and financial dimensions to create a set of rules that determine the order and values used when entering the account number.</span></span> <span data-ttu-id="40d9a-105">คุณสามารถตั้งค่าโครงสร้างทางบัญชีได้มากเท่าที่คุณต้องการสำหรับธุรกิจของคุณ</span><span class="sxs-lookup"><span data-stu-id="40d9a-105">You can set up as many account structures as you need for your business.</span></span> <span data-ttu-id="40d9a-106">โครงสร้างทางบัญชีถูกกำหนดให้กับการตั้งค่าบัญชีแยกประเภทของบริษัท ดังนั้นจึงสามารถใช้ร่วมกันได้</span><span class="sxs-lookup"><span data-stu-id="40d9a-106">The account structures are assigned to a company’s ledger setup, so they can be shared.</span></span>

<span data-ttu-id="40d9a-107">เมื่อสร้างโครงสร้างทางบัญชี จำนวนสูงสุดของเซกเมนต์คือ 11</span><span class="sxs-lookup"><span data-stu-id="40d9a-107">When creating an account structure, the maximum number of segments is 11.</span></span> <span data-ttu-id="40d9a-108">ถ้าคุณต้องการเซ็กเมนต์มากขึ้นกว่านี้ ประเมินการตั้งค่าและความต้องการของคุณอย่างถี่ถ้วน เนื่องจากจะมีผลกระทบต่อประสบการณ์ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="40d9a-108">If you need more segments than this, thoroughly evaluate your setup and requirements, as it will impact the user experience.</span></span> <span data-ttu-id="40d9a-109">พิจารณาว่า สามารถสืบทอดเซ็กเมนต์ในสถานการณ์จำลองการรายงานที่ใช้ลำดับชั้น แทนที่ในระหว่างการป้อนข้อมูล หรือโดยการใช้ฟิลด์ที่ผู้ใช้กำหนด</span><span class="sxs-lookup"><span data-stu-id="40d9a-109">Consider if a segment could be derived in a reporting scenario using a hierarchy instead of during data entry, or by using a user-defined field.</span></span> <span data-ttu-id="40d9a-110">ตัวอย่างเช่น ถ้าคุณต้องการรายงานในสถานที่ แต่คุณสามารถแสดงสถานที่ตามแผนกหรือศูนย์ต้นทุน คุณจะไม่ต้องการสถานที่เป็นมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="40d9a-110">For example, if you want to report on location, but you can figure location by department or cost center, you would not need location as a financial dimension.</span></span> <span data-ttu-id="40d9a-111">ถ้าหลังจากที่คุณทำการประเมิน ต้องมีการกำหนดมากกว่า 11 เซ็กเมนต์ คุณสามารถเพิ่มเซ็กเมนต์เพิ่มเติมได้โดยใช้กฎขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="40d9a-111">If after evaluation you do determine more than 11 segments are needed, you can add additional segments using advanced rules.</span></span>

<span data-ttu-id="40d9a-112">โครงสร้างทางบัญชีจำเป็นต้องมีบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="40d9a-112">Account structures require the main account.</span></span> <span data-ttu-id="40d9a-113">บัญชีหลักไม่ต้องเป็นเซ็กเมนต์แรกในโครงสร้าง แต่จะระบุว่าโครงสร้างทางบัญชีใดมีการใช้ในระหว่างการป้อนหมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="40d9a-113">The main account does not need to be the first segment in the structure, but it does identify what account structure is being used during the account number entry.</span></span> <span data-ttu-id="40d9a-114">ด้วยเหตุนี้ ค่าบัญชีหลักสามารถมีอยู่ได้ในโครงสร้างเดียวเท่านั้น ซึ่งถูกกำหนดให้กับบัญชีแยกประเภทเพื่อให้ไม่ทับซ้อนกัน</span><span class="sxs-lookup"><span data-stu-id="40d9a-114">Because of this, a main account value can only exist in one structure assigned to the ledger so that they do not overlap.</span></span> <span data-ttu-id="40d9a-115">หลังจากที่มีการระบุโครงสร้างทางบัญชี มีการกรองข้อมูลรายการค่าที่อนุญาตเพื่อแนะนำผู้ใช้เกี่ยวกับการเบิกสินค้าเฉพาะค่ามิติที่ถูกต้อง การลดลงของความเป็นไปได้ของรายการสมุดรายวันไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="40d9a-115">After the account structure is identified, the allowed values list is filtered to guide the user through picking only valid dimension values, decreasing the possibility of an incorrect journal entry.</span></span>

> [!NOTE] 
> <span data-ttu-id="40d9a-116">ถ้าคุณวางแผนที่จะจัดงบประมาณโดยเทียบกับมิติทางการเงิน จะต้องเป็นส่วนหนึ่งของโครงสร้างทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="40d9a-116">If you plan to budget against a financial dimension, it will need to be part of an account structure.</span></span> <span data-ttu-id="40d9a-117">การจัดงบประมาณไม่ได้ใช้กฎขั้นสูงในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="40d9a-117">Budgeting does not currently utilize advanced rules.</span></span>

## <a name="example"></a><span data-ttu-id="40d9a-118">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="40d9a-118">Example</span></span>
<span data-ttu-id="40d9a-119">เมื่อต้องการแสดงให้เห็นถึงแนวทางปฏิบัติที่ดีที่สุดสำหรับการตั้งค่าโครงสร้างทางบัญชี สมมติว่า บริษัทต้องการติดตามของบัญชีงบดุลของพวกเขา (100000..399999) ที่ระดับมิติทางการเงินของบัญชีและหน่วยธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="40d9a-119">To illustrate a best practice for setting up an account structure, let's assume that a company wants to track their balance sheet accounts (100000..399999) at the account and business unit financial dimension level.</span></span> <span data-ttu-id="40d9a-120">สำหรับบัญชีรายได้และบัญชีค่าใช้จ่าย (400000..999999) จะติดตามมิติทางการเงิน หน่วยธุรกิจ แผนก และศูนย์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="40d9a-120">For revenue and expense accounts (400000..999999), they track financial dimensions Business Unit, Department, and Cost center.</span></span> <span data-ttu-id="40d9a-121">ถ้าพวกเขาทำการขาย พวกเขายังต้องการติดตามลูกค้าด้วย</span><span class="sxs-lookup"><span data-stu-id="40d9a-121">If they make a sale, they also like to track Customer.</span></span> <span data-ttu-id="40d9a-122">โดยใช้สถานการณ์นี้ ขอแนะนำให้มีโครงสร้างทางบัญชีสองโครงสร้างที่กำหนดให้กับบัญชีแยกประเภทของบริษัท - หนึ่งโครงสร้างสำหรับบัญชีงบดุล และหนึ่งโครงสร้างสำหรับบัญชีกำไรขาดทุน</span><span class="sxs-lookup"><span data-stu-id="40d9a-122">Using this scenario, it would be recommended to have two account structures assigned to the company’s ledger - one for Balance sheet accounts, and one for Profit and Loss accounts.</span></span> <span data-ttu-id="40d9a-123">เพื่อปรับประสบการณ์ใช้งานและการตรวจสอบ ลูกค้าควรเป็นกฎขั้นสูงที่จะใช้เฉพาะเมื่อมีการใช้บัญชีการขาย</span><span class="sxs-lookup"><span data-stu-id="40d9a-123">To optimize the user experience and validation, Customer should be an advanced rule that is only used when a sales account is used.</span></span>

<span data-ttu-id="40d9a-124">**โครงสร้างบัญชีงบดุล**</span><span class="sxs-lookup"><span data-stu-id="40d9a-124">**Balance sheet account structure**</span></span>

|<span data-ttu-id="40d9a-125">บัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="40d9a-125">Main account</span></span>          | <span data-ttu-id="40d9a-126">หน่วยธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="40d9a-126">Business unit</span></span>    |
|----------------------|-----------|
|<span data-ttu-id="40d9a-127">100000..399999</span><span class="sxs-lookup"><span data-stu-id="40d9a-127">100000..399999</span></span> | <span data-ttu-id="40d9a-128">\*;” “</span><span class="sxs-lookup"><span data-stu-id="40d9a-128">\*;” “</span></span>|

<span data-ttu-id="40d9a-129">**โครงสร้างทางบัญชีกำไรขาดทุน**</span><span class="sxs-lookup"><span data-stu-id="40d9a-129">**Profit and loss account structure**</span></span>

|<span data-ttu-id="40d9a-130">บัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="40d9a-130">Main account</span></span>          | <span data-ttu-id="40d9a-131">หน่วยธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="40d9a-131">Business unit</span></span>    |<span data-ttu-id="40d9a-132">แผนก</span><span class="sxs-lookup"><span data-stu-id="40d9a-132">Department</span></span>          | <span data-ttu-id="40d9a-133">ศูนย์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="40d9a-133">Cost center</span></span>    |
|----------------------|-----------|----------------------|-----------|
|<span data-ttu-id="40d9a-134">400000..999999</span><span class="sxs-lookup"><span data-stu-id="40d9a-134">400000..999999</span></span> | <span data-ttu-id="40d9a-135">\*;” “</span><span class="sxs-lookup"><span data-stu-id="40d9a-135">\*;” “</span></span>|<span data-ttu-id="40d9a-136">\*;” “</span><span class="sxs-lookup"><span data-stu-id="40d9a-136">\*;” “</span></span>|<span data-ttu-id="40d9a-137">\*;” “</span><span class="sxs-lookup"><span data-stu-id="40d9a-137">\*;” “</span></span>|<span data-ttu-id="40d9a-138">\*;” “</span><span class="sxs-lookup"><span data-stu-id="40d9a-138">\*;” “</span></span>|

<span data-ttu-id="40d9a-139">**กฎขั้นสูงสำหรับการเพิ่มลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="40d9a-139">**Advanced rule for adding a Customer**</span></span>

<span data-ttu-id="40d9a-140">เกณฑ์: ที่ซึ่งบัญชีหลักอยู่ระหว่าง 400000 และ 499999 จากนั้น เพิ่มลูกค้า</span><span class="sxs-lookup"><span data-stu-id="40d9a-140">Criteria: Where Main account is between 400000 and 499999, then add customer.</span></span> <span data-ttu-id="40d9a-141">ไม่สามารถปล่อยให้ว่างเปล่าได้</span><span class="sxs-lookup"><span data-stu-id="40d9a-141">It cannot be left blank.</span></span>

|<span data-ttu-id="40d9a-142">ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="40d9a-142">Customer</span></span>         |
|-----------------|
|* |

<span data-ttu-id="40d9a-143">ในตัวอย่างแบบง่ายนี้ ค่าและช่องว่างทั้งหมดได้รับอนุญาต ดังนั้น \* และ “ “ จึงถูกใช้</span><span class="sxs-lookup"><span data-stu-id="40d9a-143">In this simplified example, all values and blank are allowed so \* and “ “ are used.</span></span>

## <a name="segments-and-allowed-values"></a><span data-ttu-id="40d9a-144">เซ็กเมนต์และค่าที่อนุญาต</span><span class="sxs-lookup"><span data-stu-id="40d9a-144">Segments and allowed values</span></span>
<span data-ttu-id="40d9a-145">ส่วน **เซ็กเมนต์** และ **รายละเอียดค่าที่อนุญาต** แสดงกริดเหมือนกับประสบการณ์ใช้งานสำหรับการป้อนกฎที่จะถูกติดตามเกี่ยวกับการตรวจสอบความถูกต้อง ในระหว่างการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="40d9a-145">The **Segments** and **Allowed values details** section provides a grid like experience for entering the rules that will be followed on validation during posting.</span></span> <span data-ttu-id="40d9a-146">คุณสามารถพิมพ์ลงในเซลล์ในกริดได้โดยตรง นำเข้าจาก Excel หรือใช้ส่วน **รายละเอียดค่าที่อนุญาต** เพื่อแนะนำคุณผ่านรายการนั้น</span><span class="sxs-lookup"><span data-stu-id="40d9a-146">You can type directly in the cells in the grid, import it from Excel, or use the **Allowed value details** section to guide you through it.</span></span>

<span data-ttu-id="40d9a-147">ส่วน **รายละเอียดค่าที่อนุญาต** แนะนำคุณเกี่ยวกับการสร้างเงื่อนไขโดยใช้ **ตัวดำเนินการ** เช่น ขึ้นต้นด้วย อยู่ระหว่าง รวม และอื่นๆ อีกมากมาย</span><span class="sxs-lookup"><span data-stu-id="40d9a-147">The **Allowed value details** section guides you through creating criteria using **Operators** such as begins with, is between, includes, and many others.</span></span>

<span data-ttu-id="40d9a-148">[![อนุญาตค่า](./media/account.png)](./media/account.png)</span><span class="sxs-lookup"><span data-stu-id="40d9a-148">[![Allow values](./media/account.png)](./media/account.png)</span></span> 

## <a name="more-than-7-criteria-needed"></a><span data-ttu-id="40d9a-149">จำเป็นต้องใช้เงื่อนไขมากกว่า 7 รายการ</span><span class="sxs-lookup"><span data-stu-id="40d9a-149">More than 7 criteria needed</span></span>

<span data-ttu-id="40d9a-150">ถ้าคุณมีเงื่อนไขมากกว่า 7 รายการที่จำเป็น คุณสามารถเพิ่มไปที่รายการถัดไปได้ต่อ</span><span class="sxs-lookup"><span data-stu-id="40d9a-150">If you have more than 7 criteria that are needed, you can continue adding them on the next line.</span></span> <span data-ttu-id="40d9a-151">คุณจะสังเกตเห็นว่า เมื่อทำงานในส่วน **รายละเอียดค่าที่อนุญาต** ที่เงื่อนไข **+ เพิ่มใหม่** คือไม่มีการใช้งานอีกต่อไป หลังจากป้อนเกณฑ์ที่เจ็ด</span><span class="sxs-lookup"><span data-stu-id="40d9a-151">You will notice when working in the **Allowed value details** section that the **+Add new** criteria is nt longer active after the seventh criteria is entered.</span></span> <span data-ttu-id="40d9a-152">นี่เป็นเพราะปัจจัยหลายอย่าง เช่น:</span><span class="sxs-lookup"><span data-stu-id="40d9a-152">This is due to many factors such as:</span></span> 
 - <span data-ttu-id="40d9a-153">ความกว้างคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="40d9a-153">Column width</span></span> 
 - <span data-ttu-id="40d9a-154">วิธีการจัดเก็บข้อมูล</span><span class="sxs-lookup"><span data-stu-id="40d9a-154">How the data is stored</span></span> 
 - <span data-ttu-id="40d9a-155">ประสิทธิภาพของตัวควบคุม **รายละเอียดค่าที่อนุญาต**</span><span class="sxs-lookup"><span data-stu-id="40d9a-155">Performance of the **Allowed value details** control</span></span>
 - <span data-ttu-id="40d9a-156">การใช้งาน</span><span class="sxs-lookup"><span data-stu-id="40d9a-156">Usability</span></span>  
 
<span data-ttu-id="40d9a-157">ในการดำเนินต่อเพื่อเพิ่มเงื่อนไขเพิ่มเติม คลิก **ทำซ้ำในเซ็กเมนต์** และ **ส่วนค่าที่อนุญาต**</span><span class="sxs-lookup"><span data-stu-id="40d9a-157">To continue to add additional criteria, click **Duplicate in the Segment** and **Allowed values section**.</span></span> <span data-ttu-id="40d9a-158">ซึ่งจะคัดลอกเงื่อนไขไปยังรายการใหม่</span><span class="sxs-lookup"><span data-stu-id="40d9a-158">This will copy the criteria to a new line.</span></span> <span data-ttu-id="40d9a-159">จากนั้น คุณสามารถพิมพ์เกินหรือปรับเปลี่ยนส่วน **รายละเอียดค่าที่อนุญาต** ได้</span><span class="sxs-lookup"><span data-stu-id="40d9a-159">You can then type over or modify the **Allowed value details** section.</span></span>

<span data-ttu-id="40d9a-160">(เชื่อมโยงไปยังวิดีโอที่จะถูกสร้าง)</span><span class="sxs-lookup"><span data-stu-id="40d9a-160">(LINK TO VIDEO THAT WILL BE CREATED)</span></span>

## <a name="best-practices"></a><span data-ttu-id="40d9a-161">แนวทางปฏิบัติ</span><span class="sxs-lookup"><span data-stu-id="40d9a-161">Best practices</span></span>
<span data-ttu-id="40d9a-162">เมื่อตั้งค่าโครงสร้างทางบัญชีของคุณ มีแนวทางปฏิบัติบางอย่างที่คุณสามารถทำตามได้</span><span class="sxs-lookup"><span data-stu-id="40d9a-162">When setting up your account structures there are some best practices you can follow.</span></span> <span data-ttu-id="40d9a-163">อย่างไรก็ตาม นี่คือคำแนะนำเท่านั้น ดังนั้นจึงควรพิจารณาสนทนาโดยรวมเกี่ยวกับธุรกิจ แผนเติบโต และแผนการบำรุงรักษาของคุณ เป็นส่วนหนึ่งของการสนทนานั้น</span><span class="sxs-lookup"><span data-stu-id="40d9a-163">However, this is only guidance so a holistic discussion about your business, growth plan, and maintenance plan should be considered as part of that discussion.</span></span>

- <span data-ttu-id="40d9a-164">ทำให้บัญชีหลักเป็นอันดับแรก หรือใกล้กับด้านหน้าของโครงสร้างทางบัญชีมากที่เป็นไปได้ เพื่อให้ผู้ใช้ได้รับประสบการณ์ที่แนะนำที่ดีที่สุดที่พวกเขาสามารถได้รับ ในระหว่างรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="40d9a-164">Make main account first or as close to the front of the account structure as possible, so users get the best guided experience they can during account entry.</span></span>

- <span data-ttu-id="40d9a-165">ใช้ซ้ำโครงสร้างทางบัญชีที่มากที่สุดเท่าที่เป็นไปได้ เพื่อลดการบำรุงรักษาทั่วทั้งนิติบุคคลของคุณ</span><span class="sxs-lookup"><span data-stu-id="40d9a-165">Reuse account structures as much as possible to reduce maintenance across your legal entities.</span></span>

- <span data-ttu-id="40d9a-166">สำหรับความแตกต่างทั่วทั้งนิติบุคคล ให้พิจารณาการใช้กฎขั้นสูงเพื่อให้สามารถนำโครงสร้างทางบัญชีมาใช้ใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="40d9a-166">For variations across legal entities, consider using advanced rules so that account structures can be reused.</span></span>

- <span data-ttu-id="40d9a-167">เมื่อกำหนดค่าที่อนุญาต ใช้ช่วงและอักขระพิเศษให้มากที่สุดเท่าที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="40d9a-167">When defining allowed values, use ranges and wildcards as much as possible.</span></span> <span data-ttu-id="40d9a-168">รายการนี้ไม่ได้อนุญาตให้คุณสามารถขยายและเปลี่ยนแปลงโดยไม่มีการบำรุงรักษาเท่านั้น แต่ระบบยังคงทำงานได้ดีมากขึ้นด้วยการตั้งค่าคอนฟิกนี้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="40d9a-168">This not only allows you to grow and change without maintenance, but the system also performs more ideally with this configuration.</span></span>

- <span data-ttu-id="40d9a-169">ไม่ใช่เพียงแค่ใส่เครื่องหมายดอกจันสำหรับทุกเซ็กเมนต์ในโครงสร้างทางบัญชี และจากนั้น อาศัยกฎขั้นสูงอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="40d9a-169">Do not just put an asterisk for every segment in the account structure and then solely rely on the advanced rules.</span></span> <span data-ttu-id="40d9a-170">การดำเนินการนี้อาจเป็นเรื่องยากในการจัดการ และบ่อยครั้งจะทำให้ผู้ใช้มีข้อผิดพลาดในระหว่างการบำรุงรักษาที่ทำให้ระบบไม่สามารถลงรายการบัญชีได้</span><span class="sxs-lookup"><span data-stu-id="40d9a-170">This can be difficult to manage and often leads to user error during maintenance that can make the system unable to post.</span></span>

## <a name="account-structure-activation"></a><span data-ttu-id="40d9a-171">การเปิดใช้งานโครงสร้างทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="40d9a-171">Account structure activation</span></span>
<span data-ttu-id="40d9a-172">เมื่อคุณพอใจกับการตั้งค่าใหม่ของคุณหรือการเปลี่ยนแปลงไปยังโครงสร้างทางบัญชี คุณต้องเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="40d9a-172">When you are satifisfied with your new setup or a change to an account structure, you must activate it.</span></span> <span data-ttu-id="40d9a-173">ถ้ามีการกำหนดโครงสร้างทางบัญชีให้กับบัญชีแยกประเภท การเปิดใช้งานนี้อาจเป็นกระบวนการที่รันเป็นเวลานาน เนื่องจากธุรกรรมที่ไม่ลงรายการบัญชีทั้งหมดในระบบต้องถูกซิงค์กับโครงสร้างใหม่</span><span class="sxs-lookup"><span data-stu-id="40d9a-173">If an account structure is assigned to a ledger, this activation can be a long running process, as all unposted transactions in the system must be synced to the new structure.</span></span> <span data-ttu-id="40d9a-174">ธุรกรรมที่ลงรายการบัญชีไม่ได้รับผลกระทบกับการเปลี่ยนแปลงโครงสร้างทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="40d9a-174">Posted transactions are not impacted with account structure changes.</span></span>

<span data-ttu-id="40d9a-175">สำหรับข้อมูลเพิ่มเติม ดู [วางแผนผังบัญชีของคุณ](plan-chart-of-accounts.md) [มิติทางการเงิน](financial-dimensions.md) และ [ป้อนชุดบัญชีและมิติ (ตัวควบคุมรายการที่มีการแบ่งส่วน)](enter-account-dimension-combinations-segmented-entry-control.md)</span><span class="sxs-lookup"><span data-stu-id="40d9a-175">For more information, see [Plan your chart of accounts](plan-chart-of-accounts.md), [Financial dimensions](financial-dimensions.md) and [Enter account and dimension combinations (segmented entry control)](enter-account-dimension-combinations-segmented-entry-control.md).</span></span>
