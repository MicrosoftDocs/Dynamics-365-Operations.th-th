---
title: ไม่มีพารามิเตอร์ของแผนหลักอยู่
description: เมื่อคุณพยายามยืนยันแผนการใบสั่ง คุณจะได้รับข้อความแสดงข้อผิดพลาดที่ระบุว่าไม่มีพารามิเตอร์อยู่
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d4b64af2e30109b8560d40c4c532504611528bbe
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294193"
---
# <a name="parameters-for-the-master-plan-dont-exist"></a><span data-ttu-id="4791a-103">ไม่มีพารามิเตอร์ของแผนหลักอยู่</span><span class="sxs-lookup"><span data-stu-id="4791a-103">Parameters for the master plan don't exist</span></span>

<span data-ttu-id="4791a-104">รหัสข้อผิดพลาด: SYS25368</span><span class="sxs-lookup"><span data-stu-id="4791a-104">Error code: SYS25368</span></span>

## <a name="symptoms"></a><span data-ttu-id="4791a-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="4791a-105">Symptoms</span></span>

<span data-ttu-id="4791a-106">เมื่อคุณพยายามยืนยันแผนการใบสั่ง คุณจะได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4791a-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="4791a-107">ไม่มีพารามิเตอร์สำหรับแผนหลัก %1 อยู่</span><span class="sxs-lookup"><span data-stu-id="4791a-107">Parameters for master plan %1 do not exist.</span></span>

## <a name="cause"></a><span data-ttu-id="4791a-108">สาเหตุ</span><span class="sxs-lookup"><span data-stu-id="4791a-108">Cause</span></span>

<span data-ttu-id="4791a-109">เนื่องจากปัญหาการตั้งค่าคอนฟิก ระบบไม่พบการตั้งค่าของแผนที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="4791a-109">Because of configuration issues, the system can't find the settings for the specified plan.</span></span>

## <a name="resolution"></a><span data-ttu-id="4791a-110">การแก้ปัญหา</span><span class="sxs-lookup"><span data-stu-id="4791a-110">Resolution</span></span>

- <span data-ttu-id="4791a-111">ไปที่ **การวางแผนหลัก \> การตั้งค่า \> แผน \> แผนหลัก** และตรวจสอบให้แน่ใจว่ามีแผนที่มีชื่อที่ระบุอยู่</span><span class="sxs-lookup"><span data-stu-id="4791a-111">Go to **Master planning \> Setup \> Plans \> Master plans**, and make sure that a plan that has the specified name exists.</span></span>
