---
title: สร้างรายการเมนูอุปกรณ์เคลื่อนที่สำหรับการรวมป้ายทะเบียน
description: 'กระบวนงานนี้แสดงวิธีการสร้างรายการเมนูอุปกรณ์เคลื่อนที่สำหรับงานการรวมป้ายทะเบียน '
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3f5f572461de007f137ffa7ea05c535371f95b7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977249"
---
# <a name="create-a-mobile-device-menu-item-for-license-plate-consolidation"></a><span data-ttu-id="2ad86-103">สร้างรายการเมนูอุปกรณ์เคลื่อนที่สำหรับการรวมป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="2ad86-103">Create a mobile device menu item for license plate consolidation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2ad86-104">กระบวนงานนี้แสดงวิธีการสร้างรายการเมนูอุปกรณ์เคลื่อนที่สำหรับงานการรวมป้ายทะเบียน </span><span class="sxs-lookup"><span data-stu-id="2ad86-104">This procedure shows you how to create a mobile device menu item for license plate consolidation work.</span></span> <span data-ttu-id="2ad86-105">ซึ่งช่วยให้ผู้ปฏิบัติงานคลังสินค้าสามารถรวมรายการต่างๆ ได้ในป้ายทะเบียนเดียว โดยมีรายการต่างๆ ในป้ายทะเบียนอื่นที่อยู่ในสถานที่เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="2ad86-105">This enables warehouse workers to consolidate items on one license plate with items on another license place within the same location.</span></span> <span data-ttu-id="2ad86-106">ตัวอย่างเช่น พวกเขาอาจใช้สิ่งนี้ถ้าขั้นตอนการแบ่งระยะถัดไปในใบสั่งงานทั้งสองเหมือนกัน เพื่อให้จำเป็นต้องดำเนินงานเพียงหนึ่งครั้งสำหรับสินค้าผสม</span><span class="sxs-lookup"><span data-stu-id="2ad86-106">For example, they might use this if subsequent staging steps were the same on both work orders, so that the work only needs to be performed once for the merged items.</span></span> <span data-ttu-id="2ad86-107">คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="2ad86-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="2ad86-108">โดยทั่วไปงานเหล่านี้จะถูกดำเนินการโดยผู้จัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="2ad86-108">The task would typically be carried out by a warehouse manager.</span></span> <span data-ttu-id="2ad86-109">กระบวนงานนี้ใช้สำหรับลักษณะการทำงานที่ถูกเพิ่มใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="2ad86-109">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

1. <span data-ttu-id="2ad86-110">ไปที่การจัดการคลังสินค้า > การตั้งค่า > อุปกรณ์เคลื่อนที่ > รายการเมนูอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="2ad86-110">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="2ad86-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="2ad86-111">Click New.</span></span>
3. <span data-ttu-id="2ad86-112">ในฟิลด์ชื่อเมนูสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="2ad86-112">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="2ad86-113">ในฟิลด์หัวข้อ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="2ad86-113">In the Title field, type a value.</span></span>
5. <span data-ttu-id="2ad86-114">ในฟิลด์โหมด เลือก 'ทางอ้อม'</span><span class="sxs-lookup"><span data-stu-id="2ad86-114">In the Mode field, select 'Indirect'.</span></span>
6. <span data-ttu-id="2ad86-115">ในฟิลด์รหัสกิจกรรม เลือก 'รวมป้ายทะเบียน'</span><span class="sxs-lookup"><span data-stu-id="2ad86-115">In the Activity code field, select 'Consolidate license plates'.</span></span>

