---
title: ใบสั่งซื้อที่ได้รับจริงจะไม่ปรากฏในรายงานการปิดบัญชีสินค้าคงคลัง
description: ใบสั่งซื้อที่ได้รับจริงจะไม่ปรากฏในรายงานการปิดบัญชีสินค้าคงคลังตรวจสอบปริมาณคงค้าง
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventOpenQtyCritical
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 9508d6d75d8ebee7ca10140ed4c4215d7ad1dda7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026949"
---
# <a name="physically-received-purchase-orders-dont-appear-on-the-inventory-closing-report"></a><span data-ttu-id="187c8-103">ใบสั่งซื้อที่ได้รับจริงจะไม่ปรากฏในรายงานการปิดบัญชีสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="187c8-103">Physically received purchase orders don't appear on the inventory closing report</span></span>

<span data-ttu-id="187c8-104">หมายเลข KB: 4612595</span><span class="sxs-lookup"><span data-stu-id="187c8-104">KB number: 4612595</span></span>

## <a name="symptoms"></a><span data-ttu-id="187c8-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="187c8-105">Symptoms</span></span>

<span data-ttu-id="187c8-106">ใบสั่งซื้อที่ได้รับจริงจะไม่ปรากฏในรายงานการปิดบัญชีสินค้าคงคลัง **ตรวจสอบปริมาณคงค้าง**</span><span class="sxs-lookup"><span data-stu-id="187c8-106">Physically received purchase orders don't appear on the **Check open quantities** inventory closing report.</span></span>

## <a name="resolution"></a><span data-ttu-id="187c8-107">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="187c8-107">Resolution</span></span>

<span data-ttu-id="187c8-108">รายงาน **ตรวจสอบปริมาณคงค้าง** แสดงธุรกรรมการตัดสินค้าจากคลังที่ไม่สามารถจับคู่กับการรับสต็อกที่อัปเดตทางการเงิน ณ วันที่ปิดบัญชีที่เลือก</span><span class="sxs-lookup"><span data-stu-id="187c8-108">The **Check open quantities** report shows issue transactions that can't be settled against financially updated inventory receipts as of the selected closing date.</span></span> <span data-ttu-id="187c8-109">คุณสามารถเลือกที่จะรวมการรับสินค้าตามจริงไว้ในรายงานได้</span><span class="sxs-lookup"><span data-stu-id="187c8-109">You can choose to include physical receipts on the report.</span></span> <span data-ttu-id="187c8-110">ในกรณีดังกล่าว จะมีการแสดงการรับสินค้าตามจริง หากใบรับสินค้าสามารถครอบคลุมธุรกรรมการตัดสินค้าจากคลังที่ไม่สามารถจับคู่ได้</span><span class="sxs-lookup"><span data-stu-id="187c8-110">In that case, physical receipts will be shown if they can cover the issue transactions that can't be settled.</span></span> <span data-ttu-id="187c8-111">- สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การจัดเตรียมการเรียกใช้การปิดบัญชีสินค้าคงคลัง](/dynamicsax-2012/appuser-itpro/preparing-to-run-inventory-close)</span><span class="sxs-lookup"><span data-stu-id="187c8-111">For more information, see [Preparing to run inventory close](/dynamicsax-2012/appuser-itpro/preparing-to-run-inventory-close).</span></span>
