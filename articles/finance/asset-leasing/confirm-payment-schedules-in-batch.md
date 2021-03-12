---
title: ยืนยันกำหนดการชำระเงินการเช่าสินทรัพย์ในชุดงาน
description: หัวข้อนี้จะอธิบายถึงวิธีการยืนยันกำหนดการชำระเงินหลายรายการในชุดงาน
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
ms.openlocfilehash: 9c680ea16e9f64107fde081c7e7763697356dcc1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971389"
---
# <a name="confirm-asset-leasing-payment-schedules-in-a-batch"></a><span data-ttu-id="b38d8-103">ยืนยันกำหนดการชำระเงินการเช่าสินทรัพย์ในชุดงาน</span><span class="sxs-lookup"><span data-stu-id="b38d8-103">Confirm Asset leasing payment schedules in a batch</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b38d8-104">หัวข้อนี้จะอธิบายถึงวิธีการยืนยันกำหนดการชำระเงินหลายรายการในชุดงาน</span><span class="sxs-lookup"><span data-stu-id="b38d8-104">This topic explains how to confirm multiple payment schedules in a batch.</span></span> <span data-ttu-id="b38d8-105">กำหนดการชำระเงินจะได้รับการยืนยันอย่างใดอย่างหนึ่งบนพื้นฐานของการเช่าไปยังหรือผ่านกระบวนการชุดงานการยืนยัน</span><span class="sxs-lookup"><span data-stu-id="b38d8-105">Payment schedules are confirmed either on a lease-to-lease basis or through the confirmation batch process.</span></span> <span data-ttu-id="b38d8-106">คุณสามารถลงรายการบัญชีรายการสมุดรายวันกับสัญญาเช่าที่มีกำหนดการชำระเงินที่ยืนยันแล้วเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="b38d8-106">A journal entry can be posted only against a lease that has a confirmed payment schedule.</span></span> <span data-ttu-id="b38d8-107">การยืนยันกำหนดการชำระเงินจะทำหน้าที่เป็นการอนุมัติขั้นสุดท้ายของข้อมูลทางการเงินสำหรับสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="b38d8-107">Confirmation of the payment schedule serves as a final approval of the financial information for the lease.</span></span> <span data-ttu-id="b38d8-108">การเปลี่ยนแปลงข้อมูลทางการเงินในอนาคตทั้งหมดสำหรับสัญญาเช่า เช่น การชำระเงินและเงื่อนไขระยะเวลาของสัญญาเช่าถือเป็นการปรับปรุงสัญญาเช่าและควรมีการดำเนินการในลักษณะนี้</span><span class="sxs-lookup"><span data-stu-id="b38d8-108">All future changes to the financial information for the lease, such as payments and the lease term, constitute a lease adjustment and should be processed in that way.</span></span>

<span data-ttu-id="b38d8-109">เมื่อต้องการยืนยันกำหนดการชำระเงินหลายกำหนดการ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b38d8-109">To confirm multiple payment schedules, follow these steps.</span></span>

1. <span data-ttu-id="b38d8-110">ไปที่ **การเช่าสินทรัพย์ \> ประจำงวด \> ชุดงานการยืนยัน**</span><span class="sxs-lookup"><span data-stu-id="b38d8-110">Go to **Asset leasing \> Periodic \> Confirmation batch**.</span></span>
2. <span data-ttu-id="b38d8-111">บนหน้า **ชุดงานการยืนยัน** ให้เลือก **ชุดงานการยืนยัน**</span><span class="sxs-lookup"><span data-stu-id="b38d8-111">On the **Confirmation batch** page, select **Confirmation batch**.</span></span>
3. <span data-ttu-id="b38d8-112">ในกล่องโต้ตอบที่ปรากฏขึ้น ให้กรองสำหรับสมุดบัญชีที่คุณต้องการยืนยัน</span><span class="sxs-lookup"><span data-stu-id="b38d8-112">In the dialog box that appears, filter for the books that you want to confirm.</span></span>

    - <span data-ttu-id="b38d8-113">ถ้าต้องการยืนยันหนังสือทั้งหมดในกลุ่มสัญญาเช่าเฉพาะ ให้เลือกกลุ่มในฟิลด์ **กลุ่มสัญญาเช่า**</span><span class="sxs-lookup"><span data-stu-id="b38d8-113">To confirm all the books in a specific lease group, select the group in the **Lease group** field.</span></span>
    - <span data-ttu-id="b38d8-114">เมื่อต้องการยืนยันหนังสือที่ระบุ ให้เลือกสมุดบัญชีในฟิลด์ **รหัสสมุดบัญชี**</span><span class="sxs-lookup"><span data-stu-id="b38d8-114">To confirm specific books, select the books in the **Book ID** field.</span></span>
    - <span data-ttu-id="b38d8-115">เมื่อต้องการยืนยันหนังสือทั้งหมด ให้เปิดพารามิเตอร์ **สมุดบัญชีทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="b38d8-115">To confirm all books, turn on the **For all books** parameter.</span></span>

<span data-ttu-id="b38d8-116">ข้อมูลสำหรับสมุดบัญชีที่ยืนยันใหม่จะแสดงอยู่บนหน้า **สมุดบัญชีที่ยืนยัน**</span><span class="sxs-lookup"><span data-stu-id="b38d8-116">Information for the newly confirmed books is shown on the **Confirmed books** page.</span></span> <span data-ttu-id="b38d8-117">หลังจากที่ยืนยันกำหนดการชำระเงินแล้ว คุณสามารถลงรายการบัญชีรายการสมุดรายวันการรับรู้เริ่มต้นสำหรับสัญญาเช่าได้</span><span class="sxs-lookup"><span data-stu-id="b38d8-117">After the payment schedules are confirmed, the initial recognition journal entries can be posted against the leases.</span></span>
