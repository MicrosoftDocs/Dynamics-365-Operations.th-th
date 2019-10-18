---
title: ภาพรวมของเท็มเพลตของเรกคอร์ด
description: บทความนี้แนะนำแนวคิดเกี่ยวกับเท็มเพลตเรกคอร์ด และอธิบายวิธีใช้เพื่อสร้างเรกคอร์ดที่ใช้ข้อมูลร่วมกัน
author: pvillads
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16101
ms.assetid: 61ada2d8-84c3-44bc-b4c5-516b1aeac3d1
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a8f924a5c2dad45d2006240230b85592d56e676
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180241"
---
# <a name="record-templates-overview"></a><span data-ttu-id="ca97d-103">ภาพรวมของเท็มเพลตของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="ca97d-103">Record templates overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ca97d-104">บทความนี้แนะนำแนวคิดเกี่ยวกับเท็มเพลตเรกคอร์ด และอธิบายวิธีใช้เพื่อสร้างเรกคอร์ดที่ใช้ข้อมูลร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="ca97d-104">This article introduces the concept of record templates and explains how they can be used to create records that share information.</span></span>

<span data-ttu-id="ca97d-105">เท็มเพลตเรกคอร์ดสามารถช่วยให้คุณสร้างเรกคอร์ดได้อย่างรวดเร็วมากขึ้น อย่างไรก็ตามคุณสามารถสร้างเท็มเพลตเรกคอร์ดสำหรับเรกคอร์ดบางชนิดเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="ca97d-105">Record templates can help you to create records more quickly, however you can only create record templates for some record types.</span></span>

<span data-ttu-id="ca97d-106">ตัวอย่างเช่น สมมติว่า คุณกำลังป้อนข้อมูลการเช่ารถยนต์เช่าธุรกิจขนาดเล็กที่อยู่ใน San Francisco</span><span class="sxs-lookup"><span data-stu-id="ca97d-106">For example, imagine you are entering rental information for a car rental business that is located in San Francisco.</span></span> <span data-ttu-id="ca97d-107">เนื่องจากลูกค้าส่วนใหญ่มักจะมาจากพื้นที่ San Francisco อาจเป็นบ้านพักชายทะเล เป็นการดีมากถ้าคุณสามารถกรอกค่าลงในฟิลด์ **รัฐ**, **ประเทศ**และ **เมือง** บนแบบฟอร์มค่าเช่าได้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="ca97d-107">Since most of the customers are likely to be from the San Francisco area, it would be nice if you could automatically fill in the values for the **State**, **Country**, and **City** fields on the rental form.</span></span>

> [!NOTE]
> <span data-ttu-id="ca97d-108">โดยคุณสามารถใช้เท็มเพลตเฉพาะพื้นที่ที่คุณเข้าถึงได้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="ca97d-108">You can apply templates only in areas that you have access to.</span></span> <span data-ttu-id="ca97d-109">อย่างไรก็ ชื่อเท็มเพลตทั้งหมดจะมองเห็นได้ เมื่อคุณสร้างเรกคอร์ดใหม่ และผู้ใช้อื่น ๆ ด้วยเช่นกัน ถ้าคุณกำลังสร้างเท็มเพลตที่จะพร้อมใช้งานสำหรับผู้ใช้ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="ca97d-109">However all template titles are visible to you when you create a new record, and to other users as well, if you are creating templates that will be available for all users.</span></span> <span data-ttu-id="ca97d-110">ตรวจสอบให้แน่ใจว่าคุณได้พิจารณาเรื่องนี้เมื่อคุณตั้งชื่อเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="ca97d-110">Be sure to consider this when naming templates.</span></span> <span data-ttu-id="ca97d-111">ตัวอย่างเช่น หลีกเลี่ยงการใช้ชื่อที่รวมคำ เช่น "ค่าคอมมิชชัน หากเป็นความลับที่พนักงานบางคนในบริษัทได้รับค่าคอมมิชชันตามเดือน</span><span class="sxs-lookup"><span data-stu-id="ca97d-111">For example, avoid using names that include words, such as "commission," if is confidential that some employees in the company have commission-based salaries.</span></span>

<span data-ttu-id="ca97d-112">เมื่อแม่แบบหนึ่งรายการ ขึ้นไปที่คุณสามารถเข้าถึงได้มีอยู่สำหรับแบบฟอร์มเฉพาะ และคุณพยายามที่จะสร้างเรกคอร์ดใหม่ในแบบฟอร์ม แบบ **เลือกเท็มเพลตสำหรับ** หน้าจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="ca97d-112">When one or more templates that you have access to exist for a specific form and you attempt to create a new record in the form, the **Select a template for** page is displayed.</span></span> <span data-ttu-id="ca97d-113">เมื่อคุณเลือกแม่แบบจากรายการ เรกคอร์ดใหม่จะถูกสร้างขึ้น และจะประกอบด้วยข้อมูลเริ่มต้นที่ขึ้นอยู่กับเท็มเพลตที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="ca97d-113">When you select a template from the list, the new record is created and contains default information that is based on the template that you selected.</span></span> <span data-ttu-id="ca97d-114">ถ้าคุณไม่ต้องการใช้เท็มเพลตเมื่อคุณสร้างเรกคอร์ดใหม่ เลือกกล่องกาเครื่องหมาย **ไม่ต้องถามอีก** ในหน้า **เลือกเท็มเพลตสำหรับ**</span><span class="sxs-lookup"><span data-stu-id="ca97d-114">If you do not want to use templates when you create new records, select the **Do not ask again** check box in the **Select a template for** page.</span></span> <span data-ttu-id="ca97d-115">หากต้องการให้แสดงกล่องโต้ตอบการเลือกเท็มเพลตอีกครั้ง ให้คลิกขวาที่เรกคอร์ดใดๆ คลิก **ข้อมูลของเรกคอร์ด** และจากนั้นคลิก **แสดงการเลือกเท็มเพลต**</span><span class="sxs-lookup"><span data-stu-id="ca97d-115">To display the template selection dialog box again, right-click any record, click **Record info**, and then click **Show template selection**.</span></span>
