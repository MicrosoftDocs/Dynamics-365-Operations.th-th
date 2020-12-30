---
title: ลงรายการบัญชีสมุดรายวันการปรับปรุงการเปลี่ยนแปลงในการเช่าสินทรัพย์
description: หัวข้อนี้จะอธิบายถึงฟังก์ชันการทำงานที่ช่วยให้คุณสามารถเปลี่ยนพอร์ตสัญญาเช่ากับมาตรฐานการบัญชีสัญญาเช่าใหม่ การเข้ารหัสมาตรฐานทางบัญชี หัวข้อ 842 (ASC 842) และ มาตรฐาน Financial Reporting ระหว่างประเทศ 16 (IFRS 16)
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
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4af7b9dc7a03a6d17ff34ffc726eb87e848dd785
ms.sourcegitcommit: f0f5545a8ff99583e0131f435d91c64bb68a1c38
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/30/2020
ms.locfileid: "4448626"
---
# <a name="post-transition-adjustment-journal-entries-in-asset-leasing"></a><span data-ttu-id="045a8-103">ลงรายการบัญชีสมุดรายวันการปรับปรุงการเปลี่ยนแปลงในการเช่าสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="045a8-103">Post transition adjustment journal entries in Asset leasing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="045a8-104">หัวข้อนี้จะอธิบายถึงฟังก์ชันการทำงานที่ช่วยให้คุณสามารถเปลี่ยนกลุ่มสัญญาเช่าให้กับมาตรฐานทางบัญชีสัญญาเช่าใหม่: การเข้ารหัสมาตรฐานทางบัญชี หัวข้อ 842 (ASC 842) ซึ่งเป็นมาตรฐานในการลงบัญชีที่ได้รับการรับรองโดยทั่วไปในสหรัฐอเมริกา (US GAAP) และมาตรฐาน Financial Reporting ระหว่างประเทศ 16 (IFRS 16)</span><span class="sxs-lookup"><span data-stu-id="045a8-104">This topic describes the functionality that lets you transition a lease portfolio to the new lease accounting standards: Accounting Standards Codification Topic 842 (ASC 842), which is the standard in Generally Accepted Accounting Principles in the US (US GAAP), and International Financial Reporting Standard 16 (IFRS 16).</span></span>

<span data-ttu-id="045a8-105">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าสมุดบัญชีสำหรับการเปลี่ยนไปยังมาตรฐานใหม่ ให้ดูที่ [ตั้งค่าสมุดบัญชีสัญญาเช่า](set-up-lease-books.md)</span><span class="sxs-lookup"><span data-stu-id="045a8-105">For information about how to set up a book for the transition to the new standards, see [Set up lease books](set-up-lease-books.md).</span></span>

<span data-ttu-id="045a8-106">เมื่อคุณสร้างรายการสมุดรายวันการปรับปรุงการเปลี่ยนแปลง จะมีการสร้างรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="045a8-106">When you create a transition adjustment journal entry, a journal entry is generated.</span></span> <span data-ttu-id="045a8-107">รายการนี้จะแสดงผลกระทบต่องบดุลของการบันทึกสัญญาเช่าภายใต้มาตรฐานใหม่ในวันที่นั้น</span><span class="sxs-lookup"><span data-stu-id="045a8-107">This entry reflects the balance sheet impact of recording the lease under the new standards on that date.</span></span> <span data-ttu-id="045a8-108">บัญชีสินทรัพย์ที่เหมาะสมจะถูกเดบิตสำหรับยอดเงินที่ถือครองในวันที่ดังกล่าว และมีการเครดิตบัญชีหนี้สิน</span><span class="sxs-lookup"><span data-stu-id="045a8-108">The appropriate asset account is debited for the carrying amount on that date, and the liability account is credited.</span></span> <span data-ttu-id="045a8-109">ผลต่างจะถูกเดบิตหรือเครดิตเข้าในกำไรสะสม</span><span class="sxs-lookup"><span data-stu-id="045a8-109">The difference is either debited or credited to retained earnings.</span></span>

<span data-ttu-id="045a8-110">เมื่อต้องการลงรายการบัญชีการปรับปรุงการเปลี่ยนแปลงในการปฏิบัติตามมาตรฐานการบัญชี ใหม่ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="045a8-110">To post a transition adjustment in compliance with the new accounting standards, follow these steps.</span></span>

1. <span data-ttu-id="045a8-111">บนหน้า **สรุปการเช่า** เลือกการเช่าที่จะปรับปรุง แล้วเลือก **สมุดบัญชี**</span><span class="sxs-lookup"><span data-stu-id="045a8-111">On the **Lease summary** page, select the lease, and then select **Books**.</span></span>
2. <span data-ttu-id="045a8-112">ในสมุดงาน ให้เลือก **กำหนดการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="045a8-112">In the book, select **Payment schedule**.</span></span>
3. <span data-ttu-id="045a8-113">ในกล่องโต้ตอบ **กำหนดการชำระเงิน** ให้เลือก **ยืนยัน**</span><span class="sxs-lookup"><span data-stu-id="045a8-113">In the **Payment schedule** dialog box, select **Confirm**.</span></span> <span data-ttu-id="045a8-114">จากนั้นให้ปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="045a8-114">Then close the dialog box.</span></span>
4. <span data-ttu-id="045a8-115">เลือก **การปรับปรุงการเปลี่ยนแปลง**</span><span class="sxs-lookup"><span data-stu-id="045a8-115">Select **Transition adjustment**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="045a8-116">คุณสามารถสร้างการปรับปรุงการเปลี่ยนแปลงสำหรับสมุดบัญชีสัญญาเช่าที่กำหนดให้กับสมุดบัญชีที่ฟิลด์ **สมุดบัญชีการเปลี่ยนแปลง** พร้อมใช้งานเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="045a8-116">A transition adjustment can be created only for lease books that are assigned to a book where the **Transition book** field is available.</span></span> <span data-ttu-id="045a8-117">ถ้าค่าในฟิลด์ **เริ่มต้นการเช่า** อยู่หลังวันที่เปลี่ยนแปลง ค่าในฟิลด์ **การปรับปรุงการเปลี่ยนแปลง** จะไม่มีการอัปเดต</span><span class="sxs-lookup"><span data-stu-id="045a8-117">If the value in the **Lease commencement** field is later than the transition date, the value in the **Transition adjustment** field won't be updated.</span></span>

5. <span data-ttu-id="045a8-118">ถ้าต้องการดูรายการสมุดรายวัน ให้เลือก **สมุดรายวันการเช่าสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="045a8-118">To view the journal entry, select **Asset leasing journals**.</span></span>
6. <span data-ttu-id="045a8-119">เลือกสมุดรายวันใหม่ แล้วจากนั้น เลือก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="045a8-119">Select the new journal, and then select **Post**.</span></span>
