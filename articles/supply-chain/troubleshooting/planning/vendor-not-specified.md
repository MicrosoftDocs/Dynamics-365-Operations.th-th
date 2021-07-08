---
title: ไม่ได้ระบุผู้จัดจำหน่ายเมื่อยืนยันแผนการใบสั่ง
description: เมื่อคุณพยายามยืนยันแผนการใบสั่ง คุณจะได้รับข้อความแสดงข้อผิดพลาดที่ระบุว่าไม่ได้ระบุผู้จัดจำหน่าย
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: cf41295045211f8a714194494028922d573c9e9e
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294188"
---
# <a name="vendor-isnt-specified-when-planned-orders-are-firmed"></a><span data-ttu-id="7b2f6-103">ไม่ได้ระบุผู้จัดจำหน่ายเมื่อยืนยันแผนการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="7b2f6-103">Vendor isn't specified when planned orders are firmed</span></span>

<span data-ttu-id="7b2f6-104">รหัสข้อผิดพลาด: SYS23532</span><span class="sxs-lookup"><span data-stu-id="7b2f6-104">Error code: SYS23532</span></span>

## <a name="symptoms"></a><span data-ttu-id="7b2f6-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="7b2f6-105">Symptoms</span></span>

<span data-ttu-id="7b2f6-106">เมื่อคุณพยายามยืนยันแผนการใบสั่ง คุณจะได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7b2f6-106">When you try to firm planned orders, you receive the following error message:</span></span>

> <span data-ttu-id="7b2f6-107">ไม่ได้ระบุผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="7b2f6-107">Vendor is not specified</span></span>

## <a name="resolution"></a><span data-ttu-id="7b2f6-108">การแก้ปัญหา</span><span class="sxs-lookup"><span data-stu-id="7b2f6-108">Resolution</span></span>

<span data-ttu-id="7b2f6-109">ในการระบุผู้จัดจำหน่าย ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="7b2f6-109">To specify a vendor, follow these steps.</span></span>

1. <span data-ttu-id="7b2f6-110">เปิดแผนการใบสั่งที่ขาดผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="7b2f6-110">Open the planned order that is missing a vendor.</span></span>
1. <span data-ttu-id="7b2f6-111">บนแท็บด่วน **แผนการการจัดหาวัสดุ** ในฟิลด์ **ผู้จัดจำหน่าย** ให้เลือกผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="7b2f6-111">On the **Planned supply** FastTab, in the **Vendor** field, select a vendor.</span></span>
