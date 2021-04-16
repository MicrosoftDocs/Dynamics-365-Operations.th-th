---
title: การแก้ไขปัญหาใบเสนอราคาขาย
description: หัวข้อนี้จะอธิบายวิธีการแก้ไขปัญหาที่คุณอาจพบขณะทำงานกับใบเสนอราคาขาย
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 09529ba729170be7281e2ae04008d3ba4a58e060
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824761"
---
# <a name="troubleshoot-sales-quotations"></a><span data-ttu-id="eb303-103">การแก้ไขปัญหาใบเสนอราคาขาย</span><span class="sxs-lookup"><span data-stu-id="eb303-103">Troubleshoot sales quotations</span></span>

<span data-ttu-id="eb303-104">หัวข้อนี้จะอธิบายวิธีการแก้ไขปัญหาที่คุณอาจพบขณะทำงานกับใบเสนอราคาขาย</span><span class="sxs-lookup"><span data-stu-id="eb303-104">This topic describes how to fix issues that you might encounter while you work with sales quotations.</span></span>

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a><span data-ttu-id="eb303-105">ฉันไม่สามารถเปลี่ยนแปลงปริมาณการขายของใบเสนอราคาขายสำหรับสินค้าบริการได้</span><span class="sxs-lookup"><span data-stu-id="eb303-105">I can't change the sales quantity of a sales quotation for a service item.</span></span>

### <a name="issue-description"></a><span data-ttu-id="eb303-106">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="eb303-106">Issue description</span></span>

<span data-ttu-id="eb303-107">ถ้าคุณพยายามกำหนดปริมาณการขาย (ฟิลด์ **SalesQty**) สำหรับสินค้าของประเภท *การบริการ* ในบรรทัดใบเสนอราคาขาย คุณจะได้รับข้อความแสดงข้อความต่อไปนี้: "ไม่อนุญาตให้ใช้การอัปเดตสำหรับปริมาณของฟิลด์"</span><span class="sxs-lookup"><span data-stu-id="eb303-107">If you try to set a sales quantity (**SalesQty** field) for an item of the *Service* type on a sales quotation line, you will receive the following message: "Update not allowed for field Quantity."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="eb303-108">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="eb303-108">Issue resolution</span></span>

<span data-ttu-id="eb303-109">คุณไม่สามารถกำหนดปริมาณการขายสำหรับผลิตภัณฑ์ที่เป็นสินค้าบริการได้</span><span class="sxs-lookup"><span data-stu-id="eb303-109">You can't set a sales quantity for products that are service items.</span></span> <span data-ttu-id="eb303-110">ตัวอย่างเช่น ถ้าคุณมีบริการที่จะติดตั้งสินค้า จะไม่มีการบันทึกปริมาณไว้เนื่องจากไม่มีสินค้าที่มีอยู่จริง</span><span class="sxs-lookup"><span data-stu-id="eb303-110">For example, if you offer a service to install an item, it doesn't make sense to record a quantity, because there is no physical item.</span></span> <span data-ttu-id="eb303-111">มีเพียงบริการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="eb303-111">There is only a service.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]