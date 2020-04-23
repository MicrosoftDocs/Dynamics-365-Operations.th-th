---
title: ใช้การติดตามสำหรับการกระจาย
description: บทความนี้อธิบายวิธีที่คุณสามารถใช้สืบค้นการสำรวจสาเหตุของผลลัพธ์ของการกระจายใบสั่ง
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19231
ms.assetid: 9bc9bfbe-a7a9-437b-a947-826229b0585a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 046d4f5270869542d33023b9b9c927e89f5ad40b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209524"
---
# <a name="use-tracing-for-explosion"></a><span data-ttu-id="f391a-103">ใช้การติดตามสำหรับการกระจาย</span><span class="sxs-lookup"><span data-stu-id="f391a-103">Use tracing for explosion</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f391a-104">บทความนี้อธิบายวิธีที่คุณสามารถใช้สืบค้นการสำรวจสาเหตุของผลลัพธ์ของการกระจายใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="f391a-104">This article explains how you can use tracing to explore the causes behind the outcome of an order explosion.</span></span>

<span data-ttu-id="f391a-105">เปิดใช้งานการติดตาม คุณสามารถดูข้อมูลเกี่ยวกับปัจจัยที่จัดสรรให้กับผลลัพธ์ของการกระจายของใบสั่งเฉพาะได้</span><span class="sxs-lookup"><span data-stu-id="f391a-105">By enabling tracing, you can view information about the factors that contributed to the outcome of the explosion of a particular order.</span></span> <span data-ttu-id="f391a-106">ตัวอย่างต่อไปนี้จะแสดงวิธีการใช้งานข้อมูลการติดตาม</span><span class="sxs-lookup"><span data-stu-id="f391a-106">The following examples show how you can use the tracing information:</span></span>

-   <span data-ttu-id="f391a-107">ดูความสัมพันธ์ระหว่างการดำเนินการบนแผนการใบสั่งเพื่อเพิ่มประสิทธิภาพห่วงโซ่อุปทานและการจองสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="f391a-107">View relations between the actions on planned orders to optimize the supply chain and inventory reservations.</span></span>
-   <span data-ttu-id="f391a-108">ดูความสัมพันธ์กับใบสั่งที่ได้รับการอนุมัติแล้ว</span><span class="sxs-lookup"><span data-stu-id="f391a-108">View relations to orders that are already approved.</span></span> <span data-ttu-id="f391a-109">คุณสามารถโฟกัสการยืนยันความต้องการที่ได้รับมาโดยอัตโนมัติ และจัดระดับความสำคัญของใบสั่งได้แม่นยำมากขึ้นอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="f391a-109">You can focus on automatically firming derived requirements and then prioritize orders more accurately.</span></span>
-   <span data-ttu-id="f391a-110">จำลองผลการวางแผนเพื่อตรวจสอบว่าพารามิเตอร์การวางแผนงานมีประสิทธิภาพหรือไม่</span><span class="sxs-lookup"><span data-stu-id="f391a-110">Simulate planning results to determine whether the planning parameters are optimal.</span></span>
-   <span data-ttu-id="f391a-111">ระบุวิธีกำหนดข้อมูล เช่น วันที่ผลิต ปริมาณ และระดับความสำคัญสำหรับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="f391a-111">Identify how information such as production dates, quantities, and priorities for an order were determined.</span></span>

<span data-ttu-id="f391a-112">คุณสามารถดูรายละเอียดเกี่ยวกับแผนล่วงหน้าและการดำเนินการสำหรับใบสั่งที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f391a-112">You can view details about futures and actions for a selected order.</span></span> <span data-ttu-id="f391a-113">บนหน้า **การกระจาย** รายละเอียดการติดตามจะพร้อมใช้งานบนแท็บ **คำอธิบาย** ในบานหน้าต่างด้านบน</span><span class="sxs-lookup"><span data-stu-id="f391a-113">On the **Explosion** page, tracing information is available on the **Explanation** tab in the upper pane.</span></span> <span data-ttu-id="f391a-114">การติดตามเกิดขึ้นเมื่อคุณขยายใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="f391a-114">Tracing occurs when you explode an order.</span></span> <span data-ttu-id="f391a-115">เมื่อต้องการเริ่มต้นการติดตามสำหรับใบสั่ง คลิก **อัพเดต**และเลือกกล่องกาเครื่องหมาย **เปิดใช้งานการติดตาม**</span><span class="sxs-lookup"><span data-stu-id="f391a-115">To start tracing for the order, click **Update**, and then select the **Enable trace** check box.</span></span> <span data-ttu-id="f391a-116">คุณสามารถใช้ฟิลด์ **ค้นหาข้อความ** เพื่อค้นหาล็อกสำหรับข้อมูลเฉพาะได้</span><span class="sxs-lookup"><span data-stu-id="f391a-116">You can use the **Find text** field to search the log for specific information.</span></span> <span data-ttu-id="f391a-117">ผลการค้นหาจะถูกเน้นในแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="f391a-117">Search results are highlighted in the tree.</span></span>

<a name="additional-resources"></a><span data-ttu-id="f391a-118">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="f391a-118">Additional resources</span></span>
--------

[<span data-ttu-id="f391a-119">ภาพรวมของแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="f391a-119">Master plans overview</span></span>](master-plans.md)



