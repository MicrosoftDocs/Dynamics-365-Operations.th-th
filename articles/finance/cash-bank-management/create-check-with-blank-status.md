---
title: สร้างเช็คที่มีสถานะว่างเปล่า
description: หัวข้อนี้อธิบายถึงวิธีการสร้างเช็คเปล่าสำหรับบัญชีธนาคารบนหน้าเช็ค
author: abruer
ms.date: 10/26/2017
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: BankChequeTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 21941
ms.assetid: d7e22bd8-fd0d-47e1-843f-45ab0193ff8d
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 1b01daa86055156092d035d61aad78a13349f869
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815967"
---
# <a name="create-checks-that-have-blank-status"></a><span data-ttu-id="036b5-103">สร้างเช็คที่มีสถานะว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="036b5-103">Create checks that have Blank status</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="036b5-104">หัวข้อนี้จะอธิบายถึงวิธีการสร้างเช็คเปล่า</span><span class="sxs-lookup"><span data-stu-id="036b5-104">This topic explains how to create blank checks.</span></span> <span data-ttu-id="036b5-105">ตัวอย่างเช่น คุณอาจสร้างเช็คเปล่าเพื่อลงบันทึกเช็คที่ได้รับความเสียหายและไม่สามารถใช้สำหรับการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="036b5-105">For example, you might create a blank check to record a check that has been damaged and can't be used for payment.</span></span>

<span data-ttu-id="036b5-106">บนหน้า **เช็ค** คุณสามารถดำเนินงานบำรุงรักษาสำหรับเช็ค</span><span class="sxs-lookup"><span data-stu-id="036b5-106">On the **Checks** page, you perform maintenance tasks for checks.</span></span> <span data-ttu-id="036b5-107">ตัวอย่างเช่น คุณสามารถสร้างหมายเลขเช็คใหม่และลบเช็ค</span><span class="sxs-lookup"><span data-stu-id="036b5-107">For example, you can create new check numbers and delete checks.</span></span> <span data-ttu-id="036b5-108">นอกจากนี้ คุณยังสามารถสร้างเช็คที่มีสถานะ **ว่างเปล่า**</span><span class="sxs-lookup"><span data-stu-id="036b5-108">You can also create checks that have a status of **Blank**.</span></span> <span data-ttu-id="036b5-109">หลังจากสร้างเช็คเปล่าแล้ว เช็คจะไม่สามารถลบหรือนำเช็คมาใช้ใหม่ในระบบได้</span><span class="sxs-lookup"><span data-stu-id="036b5-109">After blank checks are created, they can't be deleted or reused in the system.</span></span>

> [!NOTE]
> <span data-ttu-id="036b5-110">คุณลักษณะนี้สามารถใช้ได้ในหน้า **เช็ค** เฉพาะเมื่อคุณเปิดคุณลักษณะ **สร้างเช็คที่มีสถานะว่างเปล่าในหน้าเช็ค** ในหน้า **การจัดการคุณลักษณะ** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="036b5-110">This feature is available on the **Checks** page only if you turn on the **Create checks with a blank status on the Checks page** feature on the **Feature management** page.</span></span> <span data-ttu-id="036b5-111">หากไม่ได้เปิดคุณลักษณะนี้ เช็คที่มีสถานะ **ว่างเปล่า** จะสามารถสร้างได้จากกล่องโต้ตอบ **การชำระเงินด้วยเช็ค** ระหว่างกระบวนการสร้างการชำระเงินในบัญชีเจ้าหนี้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="036b5-111">If the feature isn't turned on, checks that have **Blank** status can be created only from the **Payment by check** dialog box during the payment generation process in Accounts payable.</span></span>

<span data-ttu-id="036b5-112">หากต้องการเปิดหน้า **เช็ค** ให้ไปที่ **การจัดการเงินสดและธนาคาร \> บัญชีธนาคาร \> บัญชีธนาคาร** จากนั้นในบานหน้าต่างการดำเนินการ บนแท็บ **จัดการการชำระเงิน** ในกลุ่ม **ข้อมูลที่เกี่ยวข้อง** ให้เลือก **เช็ค**</span><span class="sxs-lookup"><span data-stu-id="036b5-112">To open the **Checks** page, go to **Cash and bank management \> Bank accounts \> Bank accounts**, and then, on the Action Pane, on the **Manage payments** tab, in the **Related information** group, select **Checks**.</span></span> <span data-ttu-id="036b5-113">หรือไปที่ **การจัดการเงินสดและธนาคาร \> การสอบถามและรายงาน \> เช็ค**</span><span class="sxs-lookup"><span data-stu-id="036b5-113">Alternatively, go to **Cash and bank management \> Inquiries and reports \> Checks**.</span></span>

<span data-ttu-id="036b5-114">จากนั้น เพื่อสร้างเช็คที่มีสถานะ **ว่างเปล่า** ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้างเช็คเปล่า**</span><span class="sxs-lookup"><span data-stu-id="036b5-114">Then, to create checks that have **Blank** status, on the Action Pane, select **Create blank checks**.</span></span> <span data-ttu-id="036b5-115">ขณะที่ระบบกำลังสร้างเช็คเปล่า บัญชีธนาคารที่เชื่อมโยงจะใช้งานไม่ได้ชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="036b5-115">While the system is creating blank checks, the associated bank account is temporarily inactivated.</span></span> <span data-ttu-id="036b5-116">ลักษณะการทำงานนี้จะช่วยลดความเสี่ยงในการสร้างการชำระเงินในเวลาเดียวกับที่มีการสร้างเช็คเปล่า</span><span class="sxs-lookup"><span data-stu-id="036b5-116">This behavior reduces the risk that payments will be generated at the same time that blank checks are created.</span></span> <span data-ttu-id="036b5-117">เมื่อการประมวลผลเสร็จสมบูรณ์ บัญชีธนาคารที่เชื่อมโยงจะกลับมาใช้งานได้อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="036b5-117">When the processing is completed, the associated bank account is reactivated.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]