---
title: ดูผลลัพธ์ระบบอัตโนมัติของใบแจ้งหนี้ของผู้จัดจำหน่าย (พรีวิว)
description: หัวข้อนี้จะอธิบายถึงวิธีการดูสถานะของใบแจ้งหนี้ของผู้จัดจำหน่ายที่อยู่ในกระบวนการส่งไปที่ลำดับงานแบบอัตโนมัติ
author: abruer
manager: AnnBe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 65e7929e612c8465f26a2f3bc7df6f13620e5b4e
ms.sourcegitcommit: 3387595e41fb03e98bb437588f6de78794ae383f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/02/2020
ms.locfileid: "3930954"
---
# <a name="view-vendor-invoice-automation-results-preview"></a><span data-ttu-id="87ff8-103">ดูผลลัพธ์ระบบอัตโนมัติของใบแจ้งหนี้ของผู้จัดจำหน่าย (พรีวิว)</span><span class="sxs-lookup"><span data-stu-id="87ff8-103">View vendor invoice automation results (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="87ff8-104">หัวข้อนี้จะอธิบายถึงวิธีการดูสถานะของใบแจ้งหนี้ของผู้จัดจำหน่ายที่อยู่ในกระบวนการส่งไปที่ลำดับงานแบบอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="87ff8-104">This topic explains how to view the status of vendor invoices that are in the automated submit-to-workflow process.</span></span> <span data-ttu-id="87ff8-105">รายละเอียดของประวัติการทำงานอัตโนมัติถูกรักษาไว้สำหรับใบแจ้งหนี้ของผู้จัดจำหน่ายที่นำเข้าแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="87ff8-105">Details of the automation history are maintained for each imported vendor invoice.</span></span> <span data-ttu-id="87ff8-106">ทั้งนี้ขึ้นอยู่กับกระบวนการทางธุรกิจที่คุณได้ทำให้เป็นแบบอัตโนมัติ หน้า **ใบแจ้งหนี้ของผู้จัดจำหน่ายที่ค้างอยู่** แสดง **สถานะการจับคู่ใบเสร็จรับเงินแบบอัตโนมัติ** และค่า **สถานะส่งไปยังลำดับงานแบบอัตโนมัติ**</span><span class="sxs-lookup"><span data-stu-id="87ff8-106">Depending on the business processes that you've automated, the **Pending vendor invoices** page shows **Automated receipt match status** and **Automated submit to workflow status** values.</span></span> <span data-ttu-id="87ff8-107">คุณสามารถดูรายละเอียดและทำให้แผนมุ่งเน้นไปที่ใบแจ้งหนี้ที่ล้มเหลวในขั้นตอนแบบอัตโนมัติได้</span><span class="sxs-lookup"><span data-stu-id="87ff8-107">You can view the details and make a plan to focus on the invoices that failed an automated step.</span></span> <span data-ttu-id="87ff8-108">จากนั้น หลังจากที่คุณแก้ไขปัญหาแล้ว คุณสามารถดำเนินกระบวนการแบบอัตโนมัติต่อได้สำหรับใบแจ้งหนี้ที่นำเข้า</span><span class="sxs-lookup"><span data-stu-id="87ff8-108">Then, after you correct the issue, you can resume the automated process for the imported invoice.</span></span>

<span data-ttu-id="87ff8-109">ก่อนที่คุณจะสามารถแก้ไขใบแจ้งหนี้ที่ส่งแล้ว คุณต้องหยุดการประมวลผลแบบอัตโนมัติชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="87ff8-109">Before you can edit an invoice that has been submitted, you must pause the automated processing.</span></span> <span data-ttu-id="87ff8-110">ถ้าใบแจ้งหนี้ในกระบวนการส่งไปยังลำดับงานแบบอัตโนมัติต้องถูกหยุดชั่วคราว ให้ตั้งค่าฟิลด์ **รวมในการประมวลผลแบบอัตโนมัติ** เป็น **ไม่** ในหน้า **ใบแจ้งหนี้ของผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="87ff8-110">If an invoice in the automated submit-to-workflow process must be paused, set the **Include in Automated processing** field to **No** on the **Vendor invoices** page.</span></span> <span data-ttu-id="87ff8-111">จากนั้น ระบบอัตโนมัติจะไม่รันจนกว่าจะมีการตั้งค่า **รวมในการประมวลผลแบบอัตโนมัติ** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="87ff8-111">Automation then won't run until **Include in Automated processing** is set to **Yes**.</span></span> <span data-ttu-id="87ff8-112">ใบแจ้งหนี้อาจถูกหยุดชั่วคราวจากระบบอัตโนมัติต่อไป ถ้ายังไม่ได้อยู่ในระบบลำดับงานและไม่ได้ถูกใช้โดยกระบวนการแบบอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="87ff8-112">An invoice can be paused from further automation if it isn't yet in the workflow system and isn't used by the automated process.</span></span>

<span data-ttu-id="87ff8-113">ถ้าใบแจ้งหนี้ที่นำเข้าขึ้นอยู่กับกระบวนการส่งไปที่ลำดับงาน คุณสามารถดูค่า **สถานะของระบบอัตโนมัติ** บนหน้า **ใบแจ้งหนี้ของผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="87ff8-113">If an imported invoice is subject to the submit-to-workflow process, you can view its **Automation status** value on the **Vendor invoices** page.</span></span> <span data-ttu-id="87ff8-114">มีการติดตามสถานะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="87ff8-114">The following statuses are tracked:</span></span>

- <span data-ttu-id="87ff8-115">**รวมแล้ว** – กระบวนการแบบอัตโนมัติที่ถูกกำหนดไว้ในหน้า **พารามิเตอร์ของบัญชีเจ้าหนี้** กำลังรันอย่างถูกต้อง แต่ยังไม่เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="87ff8-115">**Included** – The automated processes that are defined on the **Accounts payable parameters** page are running correctly but haven't yet been completed.</span></span>
- <span data-ttu-id="87ff8-116">**หยุดชั่วคราวแล้ว** – กระบวนการแบบอัตโนมัติที่ถูกกำหนดไว้ในหน้า **พารามิเตอร์ของบัญชีเจ้าหนี้** มีการรัน แต่ล้มเหลวอย่างน้อยหนึ่งขั้นตอนในกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="87ff8-116">**Paused** – The automated processes that are defined on the **Accounts payable parameters** page have run, but at least one step in the process failed.</span></span> <span data-ttu-id="87ff8-117">นอกจากนี้ สถานะ **หยุดชั่วคราวแล้ว** ยังถูกนำไปใช้ ถ้ามีการตั้งค่าฟิลด์ **รวมในการประมวลผลแบบอัตโนมัติ** เป็น **ไม่**</span><span class="sxs-lookup"><span data-stu-id="87ff8-117">The **Paused** status is also applied if the **Include in automated processing** field is set to **No**.</span></span> <span data-ttu-id="87ff8-118">คุณสามารถดูความผิดพลาดได้โดยเลือก **ดูผลลัพธ์ล่าสุด**</span><span class="sxs-lookup"><span data-stu-id="87ff8-118">You can view the failures by selecting **View most recent results**.</span></span>
- <span data-ttu-id="87ff8-119">**ในลำดับงาน** – มีการส่งใบแจ้งหนี้ที่นำเข้าไปยังระบบลำดับงาน โดยกระบวนการส่งไปยังลำดับงานแบบอัตโนมัติหรือด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="87ff8-119">**In workflow** – The imported invoice has been submitted to the workflow system, either by the automated submit-to-workflow process or manually.</span></span>
- <span data-ttu-id="87ff8-120">**ลำดับงานที่เสร็จสมบูรณ์** – กระบวนการลำดับงานเสร็จสมบูรณ์แล้วสำหรับใบแจ้งหนี้ที่นำเข้า</span><span class="sxs-lookup"><span data-stu-id="87ff8-120">**Workflow complete** – The workflow process has been completed for the imported invoice.</span></span>
