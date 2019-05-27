---
title: ใบสั่งขายโครงการ
description: หัวข้อนี้อธิบายวิธีการสร้างใบสั่งขายตามโครงการสำหรับโครงการเวลาและวัสดุ
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 1d54c98a08dc7cccb5cafbbe401d0ce25a276c25
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/07/2019
ms.locfileid: "1529913"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="c0097-103">ใบสั่งขายโครงการสำหรับโครงการเวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="c0097-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="c0097-104">หัวข้อนี้อธิบายวิธีการสร้างใบสั่งขายสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="c0097-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="c0097-105">คุณสามารถสร้างใบสั่งขายได้เฉพาะสำหรับโครงการประเภท **เวลาและวัสดุ**</span><span class="sxs-lookup"><span data-stu-id="c0097-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="c0097-106">ถ้าโครงการเวลาและวัสดุมีแหล่งเงินทุนหลายแหล่งในสัญญาโครงการ คุณต้องเปิดใช้งานพารามิเตอร์ **อนุญาตใบสั่งขายสำหรับโครงการที่มีแหล่งเงินทุนหลายแหล่ง** บนหน้า **พารามิเตอร์การจัดการและการบัญชีโครงการ**</span><span class="sxs-lookup"><span data-stu-id="c0097-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="c0097-107">การสนับสนุนสำหรับใบสั่งขายโครงการกับแหล่งเงินทุนหลายแหล่งพร้อมใช้งานกับเริ่มตั้งแต่การนำออกใช้แอพลิเคชัน 10.0.2 และสูงกว่า</span><span class="sxs-lookup"><span data-stu-id="c0097-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="c0097-108">พารามิเตอร์เพื่อเปิดใช้งานการสนับสนุนสำหรับใบสั่งขายโครงการที่มีแหล่งเงินทุนหลายแหล่งจะถูกลบออกในเดือนเวฟการออกใช้เมษายน 2020 หลังจากนั้นฟังก์ชันจะถูกเปิดใช้งานเสมอ</span><span class="sxs-lookup"><span data-stu-id="c0097-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="c0097-109">คุณสามารถสร้างโครงการตามใบสั่งขายได้สองวิธี:</span><span class="sxs-lookup"><span data-stu-id="c0097-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="c0097-110">ไปที่ตัวโครงการเอง</span><span class="sxs-lookup"><span data-stu-id="c0097-110">Go to the project itself.</span></span> <span data-ttu-id="c0097-111">ในบานหน้าต่างการดำเนินการ เลือก **จัดการ > งานของสินค้า > ใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="c0097-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="c0097-112">ข้อมูลโครงการจะมีค่าเริ่มต้นเป็นใบสั่งขายจากโครงการ</span><span class="sxs-lookup"><span data-stu-id="c0097-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="c0097-113">ถ้าสัญญาโครงการมีแหล่งเงินทุนมากกว่าหนึ่งรายการ คุณจะต้องเลือกแหล่งเงินทุนเพื่อตั้งค่าลูกค้าสำหรับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="c0097-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="c0097-114">ถ้ามีแหล่งเงินทุนแค่รายการเดียวสำหรับโครงการ ลูกค้าจะถูกตั้งค่าโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="c0097-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="c0097-115">ไปที่หน้ารายการ **ใบสั่งขายทั้งหมด** และสร้างใบสั่งขายใหม่</span><span class="sxs-lookup"><span data-stu-id="c0097-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="c0097-116">คุณจะต้องเลือกโครงการสำหรับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="c0097-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="c0097-117">หลังจากที่เลือกโครงการ ลูกค้าจะถูกตั้งค่าจากแหล่งเงินทุนหรือคุณจะต้องเลือกแหล่งเงินทุนถ้าสัญญาโครงการมีแหล่งเงินทุนหลายแหล่ง</span><span class="sxs-lookup"><span data-stu-id="c0097-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>

