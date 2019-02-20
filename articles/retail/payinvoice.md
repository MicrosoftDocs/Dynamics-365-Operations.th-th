---
title: ตั้งค่าสถานการณ์เกี่ยวกับชำระเงินตามใบแจ้งหนี้
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิก Dynamics 365 for Retail เพื่อรองรับสถานการณ์ต่างๆ ที่เกี่ยวกับการชำระเงินตามใบแจ้งหนี้
author: josaw1
manager: AnnBe
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: b7132dc9b3c78fa04fcfc38ea72b5678ad08deb2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "302951"
---
# <a name="set-up-pay-invoice-scenarios"></a><span data-ttu-id="fdd36-103">ตั้งค่าสถานการณ์เกี่ยวกับชำระเงินตามใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="fdd36-103">Set up pay invoice scenarios</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fdd36-104">มีการขยายฟังก์ชันการชำระเงินตามใบแจ้งหนี้ใน Dynamics 365 for Retail เพื่อรองรับ:</span><span class="sxs-lookup"><span data-stu-id="fdd36-104">The Pay invoice functionality in Dynamics 365 for Retail has been expanded to support:</span></span>

- <span data-ttu-id="fdd36-105">การชำระเงินตามใบแจ้งหนี้ใบสั่งขายหลายรายการในธุรกรรม POS ธุรกรรมเดียว</span><span class="sxs-lookup"><span data-stu-id="fdd36-105">Payoff of multiple sales order invoices in a single POS transaction.</span></span>
- <span data-ttu-id="fdd36-106">การชำระเงินตามใบแจ้งหนี้ของลูกค้าหลายรายการซึ่งรวมถึงใบแจ้งหนี้ข้อความอิสระ ใบแจ้งหนี้ตามโครงการ และใบลดหนี้</span><span class="sxs-lookup"><span data-stu-id="fdd36-106">Payment of various customer invoice types including free text invoices, project-based invoices, and credit notes.</span></span>

<span data-ttu-id="fdd36-107">ในการเปิดใช้งานสถานการณ์จำลองเหล่านี้ ต้องมีการกำหนดค่าคอนฟิกโพรไฟล์ฟังก์ชันสำหรับร้านค้าตามที่กำหนดไว้ด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="fdd36-107">To enable these scenarios, the functionality profile for stores must be configured as outlined in below.</span></span>

1. <span data-ttu-id="fdd36-108">ไปที่ **การขายปลีก \> การตั้งค่าช่องทาง \> การตั้งค่า POS \> โพรไฟล์ POS \> โพรไฟล์ฟังก์ชัน** แล้วเลือกโพรไฟล์ที่เชื่อมโยงกับร้านค้าที่คุณต้องการทำการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="fdd36-108">Go to **Retail \> Channel setup \> POS setup \> POS profiles \> Functionality profiles** and select a profile that's linked to the stores that you want to make the changes for.</span></span>
2. <span data-ttu-id="fdd36-109">บนแท็บ **ฟังก์ชัน** ให้ตั้งค่าคอนฟิกพารามิเตอร์ต่อไปนี้ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="fdd36-109">On the **Functions** tab, configure the following parameters as needed.</span></span>

    - <span data-ttu-id="fdd36-110">**ใบแจ้งหนี้ของใบสั่งขาย** – เลือก **ใช่** เพื่ออนุญาตให้ผู้ใช้ชำระเงินตามใบแจ้งหนี้ของใบสั่งขายอย่างน้อยหนึ่งรายการในธุรกรรม POS ธุรกรรมเดียว</span><span class="sxs-lookup"><span data-stu-id="fdd36-110">**Sales order invoice** – Select **Yes** to allow users to pay one or more sales order-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="fdd36-111">**ใบแจ้งหนี้ข้อความอิสระ** – เลือก **ใช่** เพื่ออนุญาตให้ผู้ใช้ชำระเงินตามใบแจ้งหนี้ของข้อความอิสระอย่างน้อยหนึ่งรายการในธุรกรรม POS ธุรกรรมเดียว</span><span class="sxs-lookup"><span data-stu-id="fdd36-111">**Free text invoice** – Select **Yes** to allow users to pay one or more free text-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="fdd36-112">**ใบแจ้งหนี้ของโครงการ** – เลือก **ใช่** เพื่ออนุญาตให้ผู้ใช้ชำระเงินตามใบแจ้งหนี้ของโครงการอย่างน้อยหนึ่งรายการในธุรกรรม POS ธุรกรรมเดียว</span><span class="sxs-lookup"><span data-stu-id="fdd36-112">**Project invoice** – Select **Yes** to allow users to pay one or more project-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="fdd36-113">**ใบลดหนี้ของใบสั่งขาย** – เลือก **ใช่** เพื่ออนุญาตให้ผู้ใช้ชำระบัญชีตามใบลดหนี้ของใบสั่งขายหลายรายการเทียบกับใบแจ้งหนี้ที่เปิด หรือประมวลผลการขอคืนเงินให้กับลูกค้าสำหรับใบลดหนี้ที่เปิด</span><span class="sxs-lookup"><span data-stu-id="fdd36-113">**Sales order credit note** – Select **Yes** to allow users to settle multiple sales order-based credit notes against open invoices or process a refund to the customer for an open credit note.</span></span>

> [!NOTE]
> <span data-ttu-id="fdd36-114">การชำระเงินหรือการชำระบัญชีสำหรับยอดเงินบางส่วนยังไม่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="fdd36-114">Payment or settlement of partial amounts is not yet supported.</span></span>
