---
title: ตั้งค่าระยะใบสั่งบริการ
description: ตั้งค่าขั้นตอนใบสั่งบริการ
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9774d5f4e97d3f768366ba552e5928929bacf508
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470940"
---
# <a name="set-up-service-order-stages"></a><span data-ttu-id="e144f-103">ตั้งค่าระยะใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="e144f-103">Set up service order stages</span></span> 

[!include [banner](../includes/banner.md)]


1.  <span data-ttu-id="e144f-104">ไปที่ **การจัดการงานบริการ** \> **ตั้งค่า** \> **ใบสั่งบริการ** \> **ขั้นตอนการบริการ**</span><span class="sxs-lookup"><span data-stu-id="e144f-104">Go to **Service management** \> **Setup** \> **Service orders** \> **Service stages**.</span></span>

2.  <span data-ttu-id="e144f-105">เลือก **สร้าง** เพื่อสร้างเรกคอร์ดใหม่</span><span class="sxs-lookup"><span data-stu-id="e144f-105">Select **New** to create a new record.</span></span>

3.  <span data-ttu-id="e144f-106">ในฟิลด์ **ขั้นตอนบริการ** และ **คำอธิบาย** ให้ระบุรหัสขั้นตอนของการบริการและคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="e144f-106">In the **Service stage** and **Description** fields, specify a service stage ID and description.</span></span>

4.  <span data-ttu-id="e144f-107">เลือกพารามิเตอร์ที่เหมาะสมสำหรับขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="e144f-107">Select the appropriate parameters for the stage.</span></span>

5.  <span data-ttu-id="e144f-108">เลือกขั้นตอนหลักสำหรับขั้นตอนปัจจุบันหรือปล่อยให้ฟิลด์ **หลัก** ว่างเปล่า หากขั้นตอนอยู่ในขั้นตอนเริ่มต้นในการตั้งค่าขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="e144f-108">Select the parent stage for the current stage or leave the **Parent** field blank if the stage is the initial stage in the stage setup.</span></span>


> [!NOTE]
> <P><span data-ttu-id="e144f-109">คุณจะไม่สามารถปรับเปลี่ยนฟิลด์ <STRONG>หลัก</STRONG> ได้ หลังจากที่คุณบันทึกขั้นตอนนี้</span><span class="sxs-lookup"><span data-stu-id="e144f-109">You cannot modify the <STRONG>Parent</STRONG> field after you save the stage.</span></span> <span data-ttu-id="e144f-110">คุณสามารถลบเรกคอร์ดและสร้างเรกคอร์ดอีกครั้งด้วยการเลือกอื่นในฟิลด์ <STRONG>หลัก</STRONG> ได้แทน</span><span class="sxs-lookup"><span data-stu-id="e144f-110">Instead, you can delete the record and create the record again with a different selection in the <STRONG>Parent</STRONG> field.</span></span></P>
> <P><span data-ttu-id="e144f-111">นอกจากนี้ คุณยังสามารถสร้างขั้นตอนได้เพียงหนึ่งขั้นตอนที่มีฟิลด์ <STRONG>หลัก</STRONG> ที่่ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="e144f-111">Also, you can only create one stage with a blank <STRONG>Parent</STRONG> field.</span></span> <span data-ttu-id="e144f-112">นั่นคือ จะสามารถมีขั้นตอนเริ่มต้นได้เพียงขั้นตอนเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="e144f-112">That is, only one initial stage is permitted.</span></span></P>


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]