---
title: ชนิดคำขอการบำรุงรักษา
description: หัวข้อนี้อธิบายวิธีการตั้งค่าชนิดคำขอการบำรุงรักษาในการจัดการสินทรัพย์
author: josaw1
manager: AnnBe
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 19d529df6c8aab036de59502b4f14101e1a07707
ms.sourcegitcommit: 2c73749779274e0b0abbcb4041bbc1df0fb6d6e4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/26/2019
ms.locfileid: "1790545"
---
# <a name="maintenance-request-types"></a><span data-ttu-id="c13a0-103">ชนิดคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="c13a0-103">Maintenance request types</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="c13a0-104">ชนิดคำขอการบำรุงรักษาจะถูกใช้ในการจัดประเภทคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="c13a0-104">Maintenance request types are used to categorize maintenance requests.</span></span> <span data-ttu-id="c13a0-105">ตัวอย่างเช่น คุณอาจมีชนิดคำขอการบำรุงรักษาที่เกี่ยวข้องกับการบำรุงรักษาเชิงป้องกันและการบำรุงรักษาเชิงแก้ไข</span><span class="sxs-lookup"><span data-stu-id="c13a0-105">For example, you might have maintenance request types that are related to preventive maintenance and corrective maintenance.</span></span> <span data-ttu-id="c13a0-106">หรือคุณอาจมีชนิดคำขอการบำรุงรักษาพิเศษที่ใช้ในการจัดการการซ่อมแซมสินทรัพย์ (การซ่อมแซมคลัง)</span><span class="sxs-lookup"><span data-stu-id="c13a0-106">Or you might have a special maintenance request type that is used to manage repair of assets (depot repair).</span></span>

<span data-ttu-id="c13a0-107">ชนิดคำขอการบำรุงรักษาจะกำหนดสังกัดที่มีกลุ่มสถานะของวงจรการใช้ของคำขอการบำรุงรักษา (แบบจำลองวงจรการใช้งานของการบำรุงรักษา)</span><span class="sxs-lookup"><span data-stu-id="c13a0-107">A maintenance request type defines the affiliation with a maintenance request lifecycle state group (maintenance lifecycle model).</span></span> <span data-ttu-id="c13a0-108">แบบจำลองวงจรการใช้งานของคำขอการบำรุงรักษาจะกำหนดสถานะวงจรการใช้งานที่สามารถตั้งค่าสำหรับคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="c13a0-108">Maintenance request lifecycle models define the lifecycle states that can be set for a maintenance request.</span></span> <span data-ttu-id="c13a0-109">(ตัวอย่างของสถานะของวงจรการใช้ของคำขอการบำรุงรักษาประกอบด้วย **สร้างแล้ว** **ใช้งานอยู่** และ **สิ้นสุดแล้ว**)</span><span class="sxs-lookup"><span data-stu-id="c13a0-109">(Examples of maintenance request lifecycle states include **Created**, **Active**, and **Ended**.)</span></span>

1. <span data-ttu-id="c13a0-110">เลือก **การจัดการสินทรัพย์** \> **การตั้งค่า** \> **คำขอการบำรุงรักษา** \> **ชนิดคำขอการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="c13a0-110">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Maintenance request types**.</span></span>
2. <span data-ttu-id="c13a0-111">เลือก **สร้าง** เพื่อสร้างชนิดคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="c13a0-111">Select **New** to create a maintenance request type.</span></span>
3. <span data-ttu-id="c13a0-112">ในฟิลด์ **ชนิดคำขอการบำรุงรักษา** ให้ป้อนรหัสสำหรับชนิดคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="c13a0-112">In the **Maintenance request type** field, enter an ID for the maintenance request type.</span></span>
4. <span data-ttu-id="c13a0-113">ในฟิลด์ **ชื่อ** ป้อนชื่อ</span><span class="sxs-lookup"><span data-stu-id="c13a0-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="c13a0-114">บน FastTab **ทั่วไป** ในฟิลด์ **แบบจำลองวงจรการใช้งานของคำขอการบำรุงรักษา** ให้เลือกแบบจำลองวงจรการใช้งานของคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="c13a0-114">On the **General** FastTab, in the **Maintenance request lifecycle model** field, select a maintenance request lifecycle model.</span></span>
6. <span data-ttu-id="c13a0-115">ในฟิลด์ **ชนิดใบสั่งงาน** เลือกชนิดใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="c13a0-115">In the **Work order type** field, select a work order type.</span></span> <span data-ttu-id="c13a0-116">เมื่อคำขอการบำรุงรักษาถูกแปลงเป็นใบสั่งงาน ใบสั่งงานจะได้รับชนิดใบสั่งงานที่เกี่ยวข้องกับชนิดคำขอการบำรุงรักษาโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="c13a0-116">When a maintenance request is converted to a work order, the work order automatically gets the work order type that is related to the maintenance request type.</span></span>

<span data-ttu-id="c13a0-117">ภาพประกอบต่อไปนี้แสดงตัวอย่างของหน้า **ชนิดคำขอการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="c13a0-117">The following illustration shows an example of the **Maintenance request types** page.</span></span>

![รูปที่ 1](media/07-setup-for-requests.png)
