---
title: ตั้งค่าวิธีการชำระเงินสำหรับการหักบัญชีเงินฝากอัตโนมัติ ISO20022
description: 'กระบวนงานนี้แสดงวิธีการตั้งค่าวิธีการชำระเงินของลูกค้าสำหรับการหักบัญชีเงินฝากอัตโนมัติ ISO20022 หรือชนิดการชำระเงินอื่นๆ โดยใช้การรายงานทางอิเล็กทรอนิกส์ '
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 38afbc3a49d9020540a56e58ce51196b53d6a9e1
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143443"
---
# <a name="setup-method-of-payment-for-iso20022-direct-debit"></a><span data-ttu-id="c50d4-103">ตั้งค่าวิธีการชำระเงินสำหรับการหักบัญชีเงินฝากอัตโนมัติ ISO20022</span><span class="sxs-lookup"><span data-stu-id="c50d4-103">Setup method of payment for ISO20022 direct debit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c50d4-104">กระบวนงานนี้แสดงวิธีการตั้งค่าวิธีการชำระเงินของลูกค้าสำหรับการหักบัญชีเงินฝากอัตโนมัติ ISO20022 หรือชนิดการชำระเงินอื่นๆ โดยใช้การรายงานทางอิเล็กทรอนิกส์ </span><span class="sxs-lookup"><span data-stu-id="c50d4-104">This procedure shows how to set up the customer method of payment for ISO20022 direct debit or any other payment type using electronic reporting.</span></span> 



<span data-ttu-id="c50d4-105">ก่อนที่คุณจะทำงานนี้ให้เสร็จสมบูรณ์ คุณจะต้องตั้งค่าการตั้งค่าคอนฟิกรูปแบบการส่งออกข้อมูลและบัญชีการชำระเงินก่อน</span><span class="sxs-lookup"><span data-stu-id="c50d4-105">Before you complete this task, you must set up export format configurations and payment accounts.</span></span>



<span data-ttu-id="c50d4-106">กระบวนงานนี้ถูกสร้างขึ้นโดยใช้บริษัทข้อมูลสาธิต DEMF</span><span class="sxs-lookup"><span data-stu-id="c50d4-106">This procedure was created using the demo data company DEMF.</span></span>



<span data-ttu-id="c50d4-107">นี่คือกระบวนงานที่สามจากกระบวนงานห้ารายการที่อธิบายกระบวนการชำระเงินของลูกค้าโดยใช้การตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="c50d4-107">This is the third of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="c50d4-108">ไปที่บัญชีลูกหนี้ > การตั้งค่าการชำระเงิน > วิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="c50d4-108">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="c50d4-109">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="c50d4-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="c50d4-110">เช่น กรองข้อมูลในฟิลด์วิธีการชำระเงิน ด้วยค่า 'ELECTRONIC'</span><span class="sxs-lookup"><span data-stu-id="c50d4-110">For example, filter on the Method of payment field with a value of 'ELECTRONIC'.</span></span>
3. <span data-ttu-id="c50d4-111">คลิกแก้ไข</span><span class="sxs-lookup"><span data-stu-id="c50d4-111">Click Edit.</span></span>
4. <span data-ttu-id="c50d4-112">ในฟิลด์บัญชีการชำระเงิน ให้ระบุค่า 'DEMF OPER'</span><span class="sxs-lookup"><span data-stu-id="c50d4-112">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
5. <span data-ttu-id="c50d4-113">ขยายส่วนรูปแบบของไฟล์</span><span class="sxs-lookup"><span data-stu-id="c50d4-113">Expand the File formats section.</span></span>
6. <span data-ttu-id="c50d4-114">เลือก ใช่ ในฟิลด์รายงานอิเล็กทรอนิกส์ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="c50d4-114">Select Yes in the Generic electronic reporting field.</span></span>
7. <span data-ttu-id="c50d4-115">ในฟิลด์การตั้งค่าคอนฟิกรูปแบบการส่งออก ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="c50d4-115">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="c50d4-116">ในรายการ เลือกการหักบัญชีเงินฝากอัตโนมัติ ISO20022 (DE)</span><span class="sxs-lookup"><span data-stu-id="c50d4-116">In the list, select ISO20022 Direct debit (DE).</span></span>  <span data-ttu-id="c50d4-117">ถ้ารายการว่างเปล่า จะไม่มีการนำเข้าหรือใช้งานการตั้งค่าคอนฟิกรูปแบบการส่งออกของการชำระเงินของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="c50d4-117">If the list is empty, the customer payment export format configuration has not been imported and active.</span></span>  
8. <span data-ttu-id="c50d4-118">เลือก ใช่ ในฟิลด์ข้อตกลงที่ต้องใช้</span><span class="sxs-lookup"><span data-stu-id="c50d4-118">Select Yes in the Require mandate field.</span></span>
    * <span data-ttu-id="c50d4-119">เลือกพารามิเตอร์ข้อตกลงที่จำเป็นสำหรับรูปแบบการชำระเงินของลูกค้า ซึ่งจำเป็นต้องรวมข้อมูลข้อตกลงในข้อความการชำระเงิน เช่น การหักบัญชีเงินฝากอัตโนมัติ SEPA</span><span class="sxs-lookup"><span data-stu-id="c50d4-119">Select the Require mandate parameter for customer payment formats, which require including mandate information in the payment message, like SEPA direct debit.</span></span>  
9. <span data-ttu-id="c50d4-120">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="c50d4-120">Click Save.</span></span>

