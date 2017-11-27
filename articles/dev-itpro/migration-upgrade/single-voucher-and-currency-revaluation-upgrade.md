---
title: "การอัพเกรดใบสำคัญเดียวและการประเมินค่าใหม่ตามสกุลเงิน"
description: "บางองค์กรป้อนสมุดรายวันที่ประกอบด้วยใบสำคัญเดียวที่มีลูกค้าหรือผู้จัดจำหน่ายมากกว่าหนึ่งราย และยังเรียกใช้กระบวนการประเมินค่าใหม่ตามสกุลเงินต่างประเทศสำหรับบัญชีลูกหนี้หรือบัญชีเจ้าหนี้ หัวข้อนี้อธิบายถึงขั้นตอนที่องค์กรเหล่านี้ควรปฏิบัติตามเมื่อจะปรับรุ่นเป็น Microsoft Dynamics 365 for Operations เวอร์ชัน 1611"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7e0cd0c96ad0f30d56eefdc46a0a69160d864175
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="single-voucher-and-currency-revaluation-upgrade"></a><span data-ttu-id="1fcbc-104">การอัพเกรดใบสำคัญเดียวและการประเมินค่าใหม่ตามสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="1fcbc-104">Single voucher and currency revaluation upgrade</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1fcbc-105">บางองค์กรป้อนสมุดรายวันที่ประกอบด้วยใบสำคัญเดียวที่มีลูกค้าหรือผู้จัดจำหน่ายมากกว่าหนึ่งราย และยังเรียกใช้กระบวนการประเมินค่าใหม่ตามสกุลเงินต่างประเทศสำหรับบัญชีลูกหนี้หรือบัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="1fcbc-105">Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process.</span></span> <span data-ttu-id="1fcbc-106">หัวข้อนี้อธิบายถึงขั้นตอนที่องค์กรเหล่านี้ควรปฏิบัติตามเมื่อจะปรับรุ่นเป็น Microsoft Dynamics 365 for Operations เวอร์ชัน 1611</span><span class="sxs-lookup"><span data-stu-id="1fcbc-106">This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

<span data-ttu-id="1fcbc-107">ทำตามขั้นตอนเหล่านี้เมื่อคุณจะปรับรุ่นเป็น Microsoft Dynamics 365 for Operations เวอร์ชัน 1611</span><span class="sxs-lookup"><span data-stu-id="1fcbc-107">Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

1.  <span data-ttu-id="1fcbc-108">ก่อนที่คุณจะปรับรุ่นเป็น Dynamics 365 for Operations ให้เรียกใช้กระบวนการประเมินค่าใหม่ตามสกุลเงินต่างประเทศสำหรับบัญชีลูกหนี้และบัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="1fcbc-108">Before you upgrade to Dynamics 365 for Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="1fcbc-109">ตั้งค่าฟิลด์ **วิธีการ** เป็น **วันที่ในใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="1fcbc-109">Set the **Method** field to **Invoice date**.</span></span> <span data-ttu-id="1fcbc-110">ธุรกรรมการประเมินค่าใหม่ถูกสร้างขึ้นโดยย้อนกลับการประเมินค่าใหม่ตามสกุลเงินต่างประเทศล่าสุด</span><span class="sxs-lookup"><span data-stu-id="1fcbc-110">A revaluation transaction is created that reverses the last foreign currency revaluation.</span></span> <span data-ttu-id="1fcbc-111">ดังนั้น ธุรกรรมที่เปิดอยู่จะมีการประเมินค่าสกุลเงินทางบัญชีของต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="1fcbc-111">Therefore, the open transactions are valued at their original accounting currency.</span></span>
2.  <span data-ttu-id="1fcbc-112">อัพเกรดเป็น Dynamics 365 for Operations เวอร์ชัน 1611</span><span class="sxs-lookup"><span data-stu-id="1fcbc-112">Upgrade to Dynamics 365 for Operations version 1611.</span></span>
3.  <span data-ttu-id="1fcbc-113">เรียกใช้กระบวนการประเมินค่าตามสกุลเงินต่างประเทศสำหรับบัญชีเจ้าหนี้และบัญชีลูกหนี้อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="1fcbc-113">Run the Accounts receivable and Accounts payable foreign currency revaluation processes again.</span></span> <span data-ttu-id="1fcbc-114">จากนั้น ตั้งค่าฟิลด์ **วิธีการ** เป็น **มาตรฐาน**</span><span class="sxs-lookup"><span data-stu-id="1fcbc-114">This time, set the **Method** field to **Standard**.</span></span> <span data-ttu-id="1fcbc-115">ธุรกรรมการประเมินค่าใหม่ถูกสร้างขึ้นโดยขึ้นอยู่กับอัตราแลกเปลี่ยนปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="1fcbc-115">A new revaluation transaction is created that is based on the current exchange rates.</span></span> <span data-ttu-id="1fcbc-116">ธุรกรรมนี้จะบันทึกกำไร/ขาดทุนที่เกิดขึ้นจริงและบัญชีแยกประเภทสรุปที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="1fcbc-116">This transaction records the unrealized gain/loss and the correct summary ledger account.</span></span>





