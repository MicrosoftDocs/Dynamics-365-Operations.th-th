---
title: ตั้งค่าชื่อสมุดรายวันสัญญาเช่า
description: หัวข้อนี้จะอธิบายถึงวิธีการกำหนดชื่อสมุดรายวันสัญญาเช่า ชื่อสมุดรายวันสัญญาเช่าระบุสมุดรายวันที่มีการลงรายการบัญชีการชำระบัญชีสินทรัพย์
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 98595848593e3abd63701b52c7a67ec61288a96e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249640"
---
# <a name="set-up-lease-journal-names"></a><span data-ttu-id="944e0-104">ตั้งค่าชื่อสมุดรายวันสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="944e0-104">Set up lease journal names</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="944e0-105">ชื่อสมุดรายวันสัญญาเช่าระบุสมุดรายวันที่มีการลงรายการบัญชีธุรกรรมการเช่าสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="944e0-105">Lease journal names specify the journals that Asset leasing transactions are posted to.</span></span> <span data-ttu-id="944e0-106">เฉพาะชื่อสมุดรายวันที่ได้รับการกำหนดให้กับชนิดสมุดรายวัน **การเช่าสินทรัพย์** เท่านั้นที่จะปรากฏขึ้นในฟิลด์ **การรับรู้เริ่มต้น** และ **ชื่อสมุดรายวันรายเดือน** บนหน้า **พารามิเตอร์การเช่าสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="944e0-106">Only journal names that are assigned to the **Asset leasing** journal type appear in the **Initial Recognition** and **Monthly Journal Name** fields on the **Asset leasing parameters** page.</span></span> <span data-ttu-id="944e0-107">เฉพาะชนิดสมุดรายวัน **การบันทึกใบแจ้งหนี้ของผู้จัดจำหน่าย** เท่านั้นที่สามารถกำหนดให้กับฟิลด์ **ชื่อสมุดรายวันใบแจ้งหนี้** ได้</span><span class="sxs-lookup"><span data-stu-id="944e0-107">Only **vendor invoice recording** journal type can be assigned to the **Invoice journal name** field.</span></span>

<span data-ttu-id="944e0-108">เมื่อต้องการตั้งค่าคอนฟิกชื่อสมุดรายวันสัญญาเช่า ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="944e0-108">To configure lease journal names, follow these steps.</span></span>

1. <span data-ttu-id="944e0-109">ไปที่ **การเช่าสินทรัพย์ \> การตั้งค่า \> พารามิเตอร์การเช่าสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="944e0-109">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="944e0-110">บนแท็บ **ทั่วไป** ในฟิลด์ **ชื่อสมุดรายวันการรับรู้เริ่มต้น** และเลือกสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="944e0-110">On the **General** tab, in the **Initial recognition journal name** field, and select a journal.</span></span> <span data-ttu-id="944e0-111">รายการสมุดรายวันการรับรู้เริ่มต้นทั้งหมดจะถูกลงรายการบัญชีในชื่อสมุดรายวันนี้</span><span class="sxs-lookup"><span data-stu-id="944e0-111">All initial recognition journal entries will be posted to this journal name.</span></span>
3. <span data-ttu-id="944e0-112">ในฟิลด์ **ชื่อสมุดรายวันใบแจ้งหนี้** ให้เลือกสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="944e0-112">In the **Invoice journal name** field, select a journal.</span></span> <span data-ttu-id="944e0-113">ถ้าตัวเลือก **ชำระให้แก่ผู้จัดจำหน่าย** ตั้งค่าเป็น **ใช่** สำหรับสมุดบัญชีค่าเช่า สัญญาเช่า และใบแจ้งหนี้การชำระเงินค่าใช้จ่ายจะถูกลงรายการบัญชีในชื่อสมุดรายวันนี้</span><span class="sxs-lookup"><span data-stu-id="944e0-113">If the **Pay to vendor** option is set to **Yes** for the lease book, lease and expense payment invoices will be posted to this journal name.</span></span>
4. <span data-ttu-id="944e0-114">ในฟิลด์ **ชื่อสมุดรายวันสัญญาเช่า** ให้เลือกสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="944e0-114">In the **Lease journal name** field, select a journal.</span></span> <span data-ttu-id="944e0-115">การคิดค่าเสื่อมราคา ดอกเบี้ย และรายการที่จัดประเภทระยะสั้นทั้งหมดจะมีการลงรายการบัญชีในชื่อสมุดรายวันนี้</span><span class="sxs-lookup"><span data-stu-id="944e0-115">All depreciation, interest, and short-term reclassification entries will be posted to this journal name.</span></span> <span data-ttu-id="944e0-116">ถ้าตัวเลือก **ชำระให้แก่ผู้จัดจำหน่าย** ตั้งค่าเป็น **ไม่** สำหรับสมุดบัญชีค่าเช่า การชำระค่าเช่า และรายการการชำระเงินค่าใช้จ่ายจะถูกลงรายการบัญชีในชื่อสมุดรายวันนี้</span><span class="sxs-lookup"><span data-stu-id="944e0-116">If the **Pay to vendor** option is set to **No** for the lease book, lease payments and expense payment entries will also be posted to this journal name.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]