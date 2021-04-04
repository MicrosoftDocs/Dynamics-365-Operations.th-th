---
title: ใช้กลไกการกำหนดราคา Dynamics 365 Commerce กับ Dynamics 365 Sales
description: หัวข้อนี้จะอธิบายวิธีการใช้กลไกการกำหนดราคา Microsoft Dynamics 365 Commerce เพื่อสร้างใบเสนอราคาขายใน Dynamics 365 Sales
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: shajain
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-11-03
ms.openlocfilehash: cd784bb37eddfc74699d1070eab453a3b527201a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560284"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a><span data-ttu-id="77daa-103">ใช้กลไกการกำหนดราคา Dynamics 365 Commerce กับ Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="77daa-103">Use the Dynamics 365 Commerce pricing engine with Dynamics 365 Sales</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="77daa-104">หัวข้อนี้จะอธิบายวิธีการใช้กลไกการกำหนดราคา Microsoft Dynamics 365 Commerce เพื่อสร้างใบเสนอราคาขายใน Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="77daa-104">This topic describes how to use the Microsoft Dynamics 365 Commerce pricing engine to create sales quotations in Dynamics 365 Sales.</span></span>

<span data-ttu-id="77daa-105">กลไกการกำหนดราคา Dynamics 365 Commerce สนับสนุนสถานการณ์จำลองการกำหนดราคาสำหรับธุรกิจต่อผู้บริโภค (B2C) ส่วนมาก เช่น การกำหนดราคาในระดับร้านค้า การกำหนดราคาที่ยึดตามความภักดีและที่ยึดตามรายได้ ส่วนลดในการซื้อคละกัน ส่วนลดปริมาณ และส่วนลดจำกัด</span><span class="sxs-lookup"><span data-stu-id="77daa-105">The Dynamics 365 Commerce pricing engine supports most business-to-consumer (B2C) pricing scenarios, such as store-level pricing, affiliation-based and loyalty-based pricing, mix-and-match discounts, quantity discounts, and threshold discounts.</span></span> <span data-ttu-id="77daa-106">กลไกการกำหนดราคาจะใช้กฎที่ซับซ้อนเพื่อกำหนดราคาที่ดีที่สุดสำหรับใบเสนอราคาหรือใบสั่งที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="77daa-106">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span>

<span data-ttu-id="77daa-107">เมื่อคุณใช้ [การรวมแบบสองทิศทาง](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview) คุณมีสามตัวเลือกสำหรับความต้องการในการกำหนดราคาของคุณ</span><span class="sxs-lookup"><span data-stu-id="77daa-107">When you use [dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), you have three options for your pricing needs.</span></span> <span data-ttu-id="77daa-108">คุณสามารถใช้การกำหนดราคาแบบคงที่ที่มาจากรายการราคาใน Dynamics 365 Sales กลไกการกำหนดราคาใน Dynamics 365 Supply Chain Management หรือกลไกการกำหนดราคาใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="77daa-108">You can use the static pricing that comes from the price list in Dynamics 365 Sales, the pricing engine in Dynamics 365 Supply Chain Management, or the pricing engine in Dynamics 365 Commerce.</span></span> <span data-ttu-id="77daa-109">ในระหว่างตัวเลือกเหล่านี้ กลไกการกำหนดราคา Commerce เหมาะกับสถานการณ์ B2C ที่สุด</span><span class="sxs-lookup"><span data-stu-id="77daa-109">Among these options, the Commerce pricing engine is best suited to B2C scenarios.</span></span>

## <a name="use-the-commerce-pricing-engine-in-sales"></a><span data-ttu-id="77daa-110">ใช้กลไกการกำหนดราคา Commerce ใน Sales</span><span class="sxs-lookup"><span data-stu-id="77daa-110">Use the Commerce pricing engine in Sales</span></span>

> [!NOTE]
> <span data-ttu-id="77daa-111">ในปัจจุบัน สามารถใช้กลไกการกำหนดราคา Commerce สำหรับการสร้างใบเสนอราคาใน Sales เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="77daa-111">Currently, the Commerce pricing engine can be used only for quotation creation in the Sales.</span></span> <span data-ttu-id="77daa-112">การรวมใบสั่งขายที่มีกลไกจัดการกำหนดราคา Commerce ยังไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="77daa-112">Sales order integration with the Commerce pricing engine isn't yet available.</span></span>

<span data-ttu-id="77daa-113">เมื่อผู้ใช้เริ่มต้นใบเสนอราคาใน Sales กรอบงานการรวมแบบสองทิศทางจะคัดลอกรายละเอียดใบเสนอราคาไปยัง Commerce</span><span class="sxs-lookup"><span data-stu-id="77daa-113">When users initiate a quotation in Sales, the dual-write framework copies the quotation details to Commerce.</span></span> <span data-ttu-id="77daa-114">การเปลี่ยนแปลงใดๆ ไปยังบรรทัดใบเสนอราคาที่มีอยู่ หรือบรรทัดใบเสนอราคาที่เพิ่มใหม่ใน Sales จะถูกคัดลอกไปยัง Commerce</span><span class="sxs-lookup"><span data-stu-id="77daa-114">Any changes to existing quotation lines or any newly added quotation lines in Sales are copied to Commerce.</span></span> <span data-ttu-id="77daa-115">เมื่อผู้ใช้ต้องการใช้กลไกการกำหนดราคา Commerce เพื่อกำหนดราคาใบเสนอราคา พวกเขาสามารถเลือก **การอ้างอิงราคา** เพื่ออัปเดตราคาของใบเสนอราคา โดยใช้กลไกการกำหนดราคา commerce</span><span class="sxs-lookup"><span data-stu-id="77daa-115">When users want to use the Commerce pricing engine to price the quotation, they can select **Price quote** to update the prices of the quotation, based on the Commerce pricing engine.</span></span> <span data-ttu-id="77daa-116">จากนั้น ราคาจะถูกอัปเดตโดยอัตโนมัติในทั้ง Sales และ Commerce</span><span class="sxs-lookup"><span data-stu-id="77daa-116">Prices are then automatically updated in both Sales and Commerce.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="77daa-117">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="77daa-117">Prerequisites</span></span>

- <span data-ttu-id="77daa-118">ก่อนที่คุณจะสามารถใช้กลไกการกำหนดราคา Commerce ใน Sales ได้ คุณต้องปฏิบัติตามขั้นตอนใน [ผู้ที่มีแนวโน้มจะเป็นลูกค้าจนถึงเงินสดในการรวมแบบสองทิศทาง](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/)</span><span class="sxs-lookup"><span data-stu-id="77daa-118">Before you can use the Commerce pricing engine in Sales, you must follow the steps in [Prospect-to-cash in dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/).</span></span>
- <span data-ttu-id="77daa-119">คุณต้องปิดการประเมินข้อตกลงทางการค้าสำหรับการป้อนข้อมูลด้วยตนเองโดยปฏิบัติตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="77daa-119">You must turn off trade agreement evaluation for manual entry by following these steps:</span></span>

    1. <span data-ttu-id="77daa-120">ในสภาพแวดล้อม Commerce ของคุณ ไปที่ **บัญชีลูกหนี้ \> การตั้งค่า \> พารามิเตอร์บัญชีลูกหนี้**</span><span class="sxs-lookup"><span data-stu-id="77daa-120">In your Commerce environment, go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
    1. <span data-ttu-id="77daa-121">บนแท็บ **ราคา** บน FastTab **การประเมินข้อตกลงทางการค้า** ให้ยกเลิกการเลือกกล่องกาเครื่องหมาย **ป้อนข้อมูลด้วยตนเอง**</span><span class="sxs-lookup"><span data-stu-id="77daa-121">On the **Prices** tab, on the **Trade agreement evaluation** FastTab, clear the **Manual entry** check box.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="77daa-122">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="77daa-122">Additional resources</span></span>

[<span data-ttu-id="77daa-123">ผู้ที่มีแนวโน้มจะเป็นลูกค้าจนถึงเงินสดในการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="77daa-123">Prospect-to-cash in dual-write</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]