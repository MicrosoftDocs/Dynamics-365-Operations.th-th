---
title: ข้อผิดพลาดเมื่อลงรายการบัญชีสมุดรายวันรายงานการเสร็จงาน
description: เมื่อคุณลงรายการบัญชีสมุดรายวันรายงานการเสร็จงาน คุณจะได้รับข้อความแสดงข้อผิดพลาดที่ระบุว่าไม่สามารถลดปริมาณที่สั่งแล้วได้
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage, ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 55db7d0033dd66c1b973abf96671a20ab05d61d8
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026938"
---
# <a name="error-when-the-report-as-finished-journal-is-posted"></a><span data-ttu-id="fd3dc-103">ข้อผิดพลาดเมื่อลงรายการบัญชีสมุดรายวันรายงานการเสร็จงาน</span><span class="sxs-lookup"><span data-stu-id="fd3dc-103">Error when the Report as finished journal is posted</span></span>

<span data-ttu-id="fd3dc-104">หมายเลข KB: 4612891</span><span class="sxs-lookup"><span data-stu-id="fd3dc-104">KB number: 4612891</span></span>

## <a name="symptoms"></a><span data-ttu-id="fd3dc-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="fd3dc-105">Symptoms</span></span>

<span data-ttu-id="fd3dc-106">เมื่อคุณลงรายการบัญชีสมุดรายวัน **รายงานการเสร็จงาน** จะเกิดข้อผิดพลาด และคุณจะได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="fd3dc-106">When you post the **Report as finished** journal, an error occurs, and you receive the following error message:</span></span>

> <span data-ttu-id="fd3dc-107">ไม่สามารถลดปริมาณที่สั่งได้ เนื่องจากมีธุรกรรมสินค้าคงคลังเปิดที่มีสถานะ "สั่งแล้ว" ไม่เพียงพอ</span><span class="sxs-lookup"><span data-stu-id="fd3dc-107">Quantity ordered cannot be reduced because there are not enough open inventory transactions with the ordered status.</span></span> <span data-ttu-id="fd3dc-108">สินค้าคือ ซื้อ ได้รับแล้ว หรือลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="fd3dc-108">The items are Purchased, Received or Registered.</span></span>

<span data-ttu-id="fd3dc-109">ข้อผิดพลาดนี้จะเกิดขึ้นเฉพาะเมื่อตั้งค่าฟิลด์ **ปริมาณที่ผิดพลาด** ในบรรทัดแรกของสมุดรายวัน **รายงานการเสร็จงาน** และมีการตั้งค่าฟิลด์ **ปริมาณสินค้าที่ดี** ในบรรทัดสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="fd3dc-109">This error occurs only when the **Error quantity** field is set on the first line of the **Report as finished** journal, and the **Good quantity** field is set on the last line.</span></span> <span data-ttu-id="fd3dc-110">ถ้าตั้งค่าฟิลด์ **ปริมาณสินค้าที่ผิดพลาด** ในบรรทัดสุดท้าย จะไม่เกิดข้อผิดพลาดขึ้น</span><span class="sxs-lookup"><span data-stu-id="fd3dc-110">If the **Error quantity** field is set on the last line, no error occurs.</span></span>

## <a name="resolution"></a><span data-ttu-id="fd3dc-111">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="fd3dc-111">Resolution</span></span>

<span data-ttu-id="fd3dc-112">เมื่อต้องการป้องกันข้อผิดพลาดนี้ ให้เปิดหน้า **พารามิเตอร์การควบคุมการผลิต** และจากนั้นบนแท็บ **ทั่วไป** แล้วตั้งค่าตัวเลือก **เพิ่มปริมาณคงเหลือด้วยปริมาณที่ผิดพลาด** เป็น *ใช่*</span><span class="sxs-lookup"><span data-stu-id="fd3dc-112">To prevent this error, open the **Production control parameters** page, and then, on the **General** tab, set the **Increase remain qty with error qty** option to *Yes*.</span></span>
