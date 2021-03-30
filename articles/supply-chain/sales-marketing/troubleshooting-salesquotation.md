---
title: การแก้ไขปัญหาใบเสนอราคาขาย
description: หัวข้อนี้จะอธิบายวิธีการแก้ไขปัญหาที่คุณอาจพบขณะทำงานกับใบเสนอราคาขาย
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 9a9cc821d2fe9accad1dae210271682cdd2ce4ba
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232217"
---
# <a name="troubleshoot-sales-quotations"></a><span data-ttu-id="f61ba-103">การแก้ไขปัญหาใบเสนอราคาขาย</span><span class="sxs-lookup"><span data-stu-id="f61ba-103">Troubleshoot sales quotations</span></span>

<span data-ttu-id="f61ba-104">หัวข้อนี้จะอธิบายวิธีการแก้ไขปัญหาที่คุณอาจพบขณะทำงานกับใบเสนอราคาขาย</span><span class="sxs-lookup"><span data-stu-id="f61ba-104">This topic describes how to fix issues that you might encounter while you work with sales quotations.</span></span>

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a><span data-ttu-id="f61ba-105">ฉันไม่สามารถเปลี่ยนแปลงปริมาณการขายของใบเสนอราคาขายสำหรับสินค้าบริการได้</span><span class="sxs-lookup"><span data-stu-id="f61ba-105">I can't change the sales quantity of a sales quotation for a service item.</span></span>

### <a name="issue-description"></a><span data-ttu-id="f61ba-106">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="f61ba-106">Issue description</span></span>

<span data-ttu-id="f61ba-107">ถ้าคุณพยายามกำหนดปริมาณการขาย (ฟิลด์ **SalesQty**) สำหรับสินค้าของประเภท *การบริการ* ในบรรทัดใบเสนอราคาขาย คุณจะได้รับข้อความแสดงข้อความต่อไปนี้: "ไม่อนุญาตให้ใช้การอัปเดตสำหรับปริมาณของฟิลด์"</span><span class="sxs-lookup"><span data-stu-id="f61ba-107">If you try to set a sales quantity (**SalesQty** field) for an item of the *Service* type on a sales quotation line, you will receive the following message: "Update not allowed for field Quantity."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f61ba-108">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="f61ba-108">Issue resolution</span></span>

<span data-ttu-id="f61ba-109">คุณไม่สามารถกำหนดปริมาณการขายสำหรับผลิตภัณฑ์ที่เป็นสินค้าบริการได้</span><span class="sxs-lookup"><span data-stu-id="f61ba-109">You can't set a sales quantity for products that are service items.</span></span> <span data-ttu-id="f61ba-110">ตัวอย่างเช่น ถ้าคุณมีบริการที่จะติดตั้งสินค้า จะไม่มีการบันทึกปริมาณไว้เนื่องจากไม่มีสินค้าที่มีอยู่จริง</span><span class="sxs-lookup"><span data-stu-id="f61ba-110">For example, if you offer a service to install an item, it doesn't make sense to record a quantity, because there is no physical item.</span></span> <span data-ttu-id="f61ba-111">มีเพียงบริการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f61ba-111">There is only a service.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]