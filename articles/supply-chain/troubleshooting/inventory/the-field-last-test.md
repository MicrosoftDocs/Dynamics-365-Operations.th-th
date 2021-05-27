---
title: ฟิลด์วันที่ทดสอบล่าสุดไม่มีการอัเดตเมื่อสร้างใบสั่งตรวจสอบคุณภาพหลายใบ
description: ฟิลด์วันที่ทดสอบล่าสุดไม่มีการอัเดตเมื่อสร้างใบสั่งตรวจสอบคุณภาพหลายใบ
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f796bdaa88d32b1c58dd8a4bca19f0ce4f3943d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026960"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a><span data-ttu-id="5f564-103">ฟิลด์วันที่ทดสอบล่าสุดไม่มีการอัเดตเมื่อสร้างใบสั่งตรวจสอบคุณภาพหลายใบ</span><span class="sxs-lookup"><span data-stu-id="5f564-103">The Last tested date field isn't updated when multiple quality orders are created</span></span>

<span data-ttu-id="5f564-104">หมายเลข KB: 4612803</span><span class="sxs-lookup"><span data-stu-id="5f564-104">KB number: 4612803</span></span>

## <a name="symptoms"></a><span data-ttu-id="5f564-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="5f564-105">Symptoms</span></span>

<span data-ttu-id="5f564-106">ฟิลด์ **วันที่ทดสอบล่าสุด** ไม่มีการอัเดตเมื่อสร้างใบสั่งตรวจสอบคุณภาพหลายใบ</span><span class="sxs-lookup"><span data-stu-id="5f564-106">The **Last tested date** field isn't updated when multiple quality orders are created.</span></span>

## <a name="resolution"></a><span data-ttu-id="5f564-107">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="5f564-107">Resolution</span></span>

<span data-ttu-id="5f564-108">ระบบมีการทำงานตามที่ออกแบบ</span><span class="sxs-lookup"><span data-stu-id="5f564-108">The system is behaving as designed.</span></span> <span data-ttu-id="5f564-109">วันที่ทดสอบล่าสุดไม่เกี่ยวข้องกับใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="5f564-109">The last tested date isn't related to quality orders.</span></span> <span data-ttu-id="5f564-110">โดยจะจัดเก็บวันที่ที่สินค้าเสร็จสมบูรณ์ที่ซื้อหรือผลิตครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="5f564-110">It stores the date when the finished goods were first purchased or manufactured.</span></span> <span data-ttu-id="5f564-111">วันที่นี้จะใช้ในการคํานวณวันที่แนะนําอายุการเก็บสินค้า</span><span class="sxs-lookup"><span data-stu-id="5f564-111">This date is used to calculate the shelf life advice date.</span></span>
