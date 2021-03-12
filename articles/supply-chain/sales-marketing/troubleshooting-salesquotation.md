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
ms.openlocfilehash: 98011dbf22ff55b7651ce63557fa4a360130b6af
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974771"
---
# <a name="troubleshoot-sales-quotations"></a><span data-ttu-id="d5bf4-103">การแก้ไขปัญหาใบเสนอราคาขาย</span><span class="sxs-lookup"><span data-stu-id="d5bf4-103">Troubleshoot sales quotations</span></span>

<span data-ttu-id="d5bf4-104">หัวข้อนี้จะอธิบายวิธีการแก้ไขปัญหาที่คุณอาจพบขณะทำงานกับใบเสนอราคาขาย</span><span class="sxs-lookup"><span data-stu-id="d5bf4-104">This topic describes how to fix issues that you might encounter while you work with sales quotations.</span></span>

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a><span data-ttu-id="d5bf4-105">ฉันไม่สามารถเปลี่ยนแปลงปริมาณการขายของใบเสนอราคาขายสำหรับสินค้าบริการได้</span><span class="sxs-lookup"><span data-stu-id="d5bf4-105">I can't change the sales quantity of a sales quotation for a service item.</span></span>

### <a name="issue-description"></a><span data-ttu-id="d5bf4-106">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="d5bf4-106">Issue description</span></span>

<span data-ttu-id="d5bf4-107">ถ้าคุณพยายามกำหนดปริมาณการขาย (ฟิลด์ **SalesQty**) สำหรับสินค้าของประเภท *การบริการ* ในบรรทัดใบเสนอราคาขาย คุณจะได้รับข้อความแสดงข้อความต่อไปนี้: "ไม่อนุญาตให้ใช้การอัปเดตสำหรับปริมาณของฟิลด์"</span><span class="sxs-lookup"><span data-stu-id="d5bf4-107">If you try to set a sales quantity (**SalesQty** field) for an item of the *Service* type on a sales quotation line, you will receive the following message: "Update not allowed for field Quantity."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="d5bf4-108">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="d5bf4-108">Issue resolution</span></span>

<span data-ttu-id="d5bf4-109">คุณไม่สามารถกำหนดปริมาณการขายสำหรับผลิตภัณฑ์ที่เป็นสินค้าบริการได้</span><span class="sxs-lookup"><span data-stu-id="d5bf4-109">You can't set a sales quantity for products that are service items.</span></span> <span data-ttu-id="d5bf4-110">ตัวอย่างเช่น ถ้าคุณมีบริการที่จะติดตั้งสินค้า จะไม่มีการบันทึกปริมาณไว้เนื่องจากไม่มีสินค้าที่มีอยู่จริง</span><span class="sxs-lookup"><span data-stu-id="d5bf4-110">For example, if you offer a service to install an item, it doesn't make sense to record a quantity, because there is no physical item.</span></span> <span data-ttu-id="d5bf4-111">มีเพียงบริการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="d5bf4-111">There is only a service.</span></span>

