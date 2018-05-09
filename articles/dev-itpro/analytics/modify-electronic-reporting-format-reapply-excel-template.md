---
title: "แก้ไขรูปแบบการรายงานทางอิเล็กทรอนิกส์ด้วยการใช้เท็มเพลต Microsoft Excel"
description: "หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีที่คุณสามารถแก้ไขรูปแบบการรายงานอิเล็กทรอนิกส์ (ER) ที่ถูกใช้ในการสร้างเอกสารทางธุรกิจ โดยการนำเท็มเพลต Excel ที่แก้ไขไปใช้ใหม่"
author: NickSelin
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 7df2c6e86975a35cd97fabad4d96fb1319d2b6ce
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---
# <a name="modify-an-electronic-reporting-format-by-reapplying-a-microsoft-excel-template"></a><span data-ttu-id="d5d8e-103">แก้ไขรูปแบบการรายงานทางอิเล็กทรอนิกส์ด้วยการใช้เท็มเพลต Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="d5d8e-103">Modify an Electronic reporting format by reapplying a Microsoft Excel template</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d5d8e-104">เครื่องมือการรายงานทางอิเล็กทรอนิกส์ (ER) จะถูกใช้ในการสร้างเอกสารทางธุรกิจในรูปแบบอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d5d8e-104">The Electronic reporting (ER) tool is used to generate business documents in an electronic format.</span></span> <span data-ttu-id="d5d8e-105">ในการสร้างเอกสารทางธุรกิจ คุณต้องสร้างรูปแบบ ER และจากนั้นใช้ตัวออกแบบ ER เพื่อกำหนดโครงร่างของเอกสารทางธุรกิจ และระบุข้อมูลที่ควรรวมอยู่ในตาราง</span><span class="sxs-lookup"><span data-stu-id="d5d8e-105">To generate a business document, you must create an ER format, and then use the ER designer to define the layout of the business document and specify the data that should be included in it.</span></span> <span data-ttu-id="d5d8e-106">จากนั้นคุณสามารถรันรูปแบบ ER ได้ เพื่อสร้างเอกสารทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="d5d8e-106">You can then run the ER format to generate the business document.</span></span>

<span data-ttu-id="d5d8e-107">เครื่องมือ ER สามารถใช้ในการสร้างเอกสารธุรกิจให้เป็นไฟล์ Microsoft Excel ได้</span><span class="sxs-lookup"><span data-stu-id="d5d8e-107">The ER tool can be used to generate business documents as Microsoft Excel files.</span></span> <span data-ttu-id="d5d8e-108">คุณสามารถใช้เอกสาร Excel เป็นเท็มเพลตสำหรับเอกสารเหล่านี้ได้</span><span class="sxs-lookup"><span data-stu-id="d5d8e-108">You can use an Excel document as a template for these documents.</span></span> <span data-ttu-id="d5d8e-109">เมื่อต้องการกำหนดโครงร่างของเอกสารในตัวออกแบบ ER คุณสามารถนำเข้าเนื้อหาของเอกสาร Excel ที่คุณต้องการใช้เป็นเท็มเพลตลงในรูปแบบ ER ที่กำหนดได้</span><span class="sxs-lookup"><span data-stu-id="d5d8e-109">To define the document layout in the ER designer, you can import the contents of the Excel document that you want to use as a template into the defined ER format.</span></span> <span data-ttu-id="d5d8e-110">สำหรับรายละเอียดเพิ่มเติม และเพื่อฝึกฝนสถานการณ์จำลองนี้ เล่นคู่มืองาน **ER ออกแบบการตั้งค่าคอนฟิกสำหรับการสร้างรายงานในรูปแบบ OPENXML** (ส่วนหนึ่งของ 7.5.4.3 จัดหา/พัฒนาบริการด้านไอที/องค์ประกอบโซลูชัน (10677) กระบวนการทางธุรกิจ)</span><span class="sxs-lookup"><span data-stu-id="d5d8e-110">For more details, and to practice this scenario, play the task guide **ER Design a configuration for generating reports in OPENXML format** (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span>

<span data-ttu-id="d5d8e-111">ถ้าคุณแก้ไขเอกสาร Excel ที่ถูกใช้เป็นเท็มเพลตสำหรับเอกสารทางธุรกิจ ฟังก์ชัน ER ใหม่ช่วยให้คุณสามารถนำเท็มเพลตที่ปรับปรุงแล้วไปใช้กับรูปแบบ ER ได้</span><span class="sxs-lookup"><span data-stu-id="d5d8e-111">If you edit the Excel document that is used as a template for a business document, new ER functionality lets you reapply the updated template to the ER format.</span></span> <span data-ttu-id="d5d8e-112">จากนั้น รูปแบบ ER ได้รับการปรับปรุงเพื่อให้ได้สอดคล้องกับเท็มเพลตที่มีการอัพเดต</span><span class="sxs-lookup"><span data-stu-id="d5d8e-112">The ER format is then updated so that it adheres to the updated template.</span></span> <span data-ttu-id="d5d8e-113">สำหรับรายละเอียดเพิ่มเติมเกี่ยวกับฟังก์ชันนี้ เล่นคู่มืองาน **ER ปรับเปลี่ยนรูปแบบตามการนำเท็มเพลต Excel ไปใช้** (ส่วนหนึ่งของ 7.5.5.3 บริการ/โซลูชัน IT รับ/การจัดทำคอมโพเนนต์ (10683) กระบวนการทางธุรกิจ)</span><span class="sxs-lookup"><span data-stu-id="d5d8e-113">For more details about this functionality, play the task guide **ER Modify a format by reapplying an Excel template** (part of the 7.5.5.3 Acquire/Develop IT service/solution components (10683) business process).</span></span> <span data-ttu-id="d5d8e-114">ในขั้นตอนคู่มืองานที่คุณนำเข้าเท็มเพลตที่อัพเดตแล้ว ใช้เท็มเพลตที่อัพเดตแล้วของแฟ้ม Excel การชำระเงิน SampleVendPaymWsReport2 เป็นเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="d5d8e-114">In the task guide step where you import an updated template, use the modified template of the Payment Report Excel file, SampleVendPaymWsReport2, as a template.</span></span>

