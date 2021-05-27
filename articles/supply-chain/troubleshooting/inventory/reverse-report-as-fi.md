---
title: การกลับรายการการรายงานการเสร็จงานสร้างธุรกรรมที่เปิดค้างไว้ที่ไม่คาดคิด
description: การกลับรายการการรายงานการเสร็จงานที่เลือกจะสร้างธุรกรรมที่เปิดค้างไว้ซึ่งปริมาณที่กลับรายการมีมิติสินค้าคงคลังเดียวกันกับธุรกรรมที่กลับรายการ
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ea9044a9008e766c7fc92f98e27cfb91076f5b44
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026961"
---
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a><span data-ttu-id="8227d-103">การกลับรายการการรายงานการเสร็จงานสร้างธุรกรรมที่เปิดค้างไว้ที่ไม่คาดคิด</span><span class="sxs-lookup"><span data-stu-id="8227d-103">Reversal of reporting as finished creates an unexpected open transaction</span></span>

<span data-ttu-id="8227d-104">หมายเลข KB: 4612469</span><span class="sxs-lookup"><span data-stu-id="8227d-104">KB number: 4612469</span></span>

## <a name="symptoms"></a><span data-ttu-id="8227d-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="8227d-105">Symptoms</span></span>

<span data-ttu-id="8227d-106">หากคุณกลับรายการการรายงานการเสร็จงานที่เลือก ระบบจะสร้างธุรกรรมที่เปิดค้างไว้ซึ่งปริมาณที่กลับรายการมีมิติสินค้าคงคลังเดียวกันกับธุรกรรมที่กลับรายการ</span><span class="sxs-lookup"><span data-stu-id="8227d-106">If you reverse reporting as finished that has marking, the system creates an open transaction where the reversed quantity has the same inventory dimensions as the transaction that was reversed.</span></span>

## <a name="resolution"></a><span data-ttu-id="8227d-107">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="8227d-107">Resolution</span></span>

<span data-ttu-id="8227d-108">เมื่อคุณกลับรายการการดําเนินงานรายงานการเสร็จงาน มิติสินค้าคงคลังจะเริ่มต้นจากสมุดรายวันการผลิต</span><span class="sxs-lookup"><span data-stu-id="8227d-108">When you reverse a report-as-finished operation, the inventory dimension is initialized from the production journal.</span></span> <span data-ttu-id="8227d-109">ดังนั้นจึงได้รับหมายเลขชุดงาน</span><span class="sxs-lookup"><span data-stu-id="8227d-109">Therefore, it gets the batch number.</span></span> <span data-ttu-id="8227d-110">เนื่องจากการทำเครื่องหมาย ธุรกรรมใบสั่งขายจะสืบทอดหมายเลขชุดงาน</span><span class="sxs-lookup"><span data-stu-id="8227d-110">Because of marking, the sales order transactions will inherit the batch number.</span></span>

<span data-ttu-id="8227d-111">มิติสามารถรีเซ็ตได้เมื่อลงรายการบัญชีการรายงานการเสร็จงาน</span><span class="sxs-lookup"><span data-stu-id="8227d-111">The dimension can be reset when the reporting as finished is posted.</span></span>
