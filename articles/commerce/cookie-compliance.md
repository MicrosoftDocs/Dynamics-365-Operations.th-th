---
title: การปฏิบัติตามกฎระเบียบคุกกี้
description: หัวข้อนี้อธิบายถึงการพิจารณาสำหรับการปฏิบัติตามข้อกำหนดคุกกี้และนโยบายเริ่มต้นที่รวมอยู่ใน Microsoft Dynamics 365 Commerce
author: BrianShook
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 38f8265f3a22da3b910ccec1607e382ff861afb1
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/09/2020
ms.locfileid: "2946090"
---
# <a name="cookie-compliance"></a><span data-ttu-id="e2b84-103">ดูการปฏิบัติตามข้อกำหนดคุกกี้</span><span class="sxs-lookup"><span data-stu-id="e2b84-103">Cookie compliance</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="e2b84-104">หัวข้อนี้อธิบายถึงการพิจารณาสำหรับการปฏิบัติตามข้อกำหนดคุกกี้และนโยบายเริ่มต้นที่รวมอยู่ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="e2b84-104">This topic describes considerations for cookie compliance and the default policies that are included in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e2b84-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="e2b84-105">Overview</span></span>

<span data-ttu-id="e2b84-106">ความเป็นส่วนตัวเป็นปัจจัยสำคัญเมื่อใดก็ตามที่มีการใช้เทคโนโลยีการติดตามใดๆ ที่มีผลต่อลูกค้าอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="e2b84-106">Privacy is an important factor whenever any tracking technologies that affect e-Commerce customers are used.</span></span> <span data-ttu-id="e2b84-107">เนื่องจากมาตรฐานการปฏิบัติตามข้อกำหนดด้านความเป็นส่วนตัว เช่น ข้อบังคับทั่วไปเกี่ยวกับการคุ้มครองข้อมูล (GDPR) ในสหภาพยุโรป (EU) จะต้องพิจารณาหลักเกณฑ์ความเป็นส่วนตัวอิเล็กทรอนิกส์สำหรับเว็บไซต์ใดๆ ที่มีการใช้งานอยู่ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="e2b84-107">Because of privacy compliance standards such as the General Data Protection Regulation (GDPR) in the European Union (EU), electronic privacy guidelines must be considered for any site that is active today.</span></span> <span data-ttu-id="e2b84-108">เนื่องจากไซต์อีคอมเมิร์ซฃจำนวนมากสามารถเข้าถึงได้ทั่วโลกโดยค่าเริ่มต้น คุณจึงควรตรวจสอบมาตรฐานการปฏิบัติตามกฎระเบียบสำหรับไซต์อีคอมเมิร์ซของคุณ</span><span class="sxs-lookup"><span data-stu-id="e2b84-108">Because many e-Commerce sites are globally accessible by default, it's important that you review the compliance standards for your e-Commerce site.</span></span>

<span data-ttu-id="e2b84-109">หากต้องการเรียนรู้เพิ่มเติมเกี่ยวกับหลักการพื้นฐานที่ Microsoft ใช้สำหรับการปฏิบัติตามข้อกำหนดของคุกกี้ ให้ไปที่ [ศูนย์ความเชื่อถือของ Microsoft](https://www.microsoft.com/trust-center)</span><span class="sxs-lookup"><span data-stu-id="e2b84-109">To learn more about the basic principles that Microsoft uses for cookie compliance, visit the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="e2b84-110">นอกจากนี้คุณยังสามารถรับข้อมูลเพิ่มเติมเกี่ยวกับพื้นที่ของการปฏิบัติตามกฎระเบียบและความเป็นส่วนตัวได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="e2b84-110">On that site, you can also get more information about areas of compliance and privacy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e2b84-111">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="e2b84-111">Additional resources</span></span>

[<span data-ttu-id="e2b84-112">คุณลักษณะและความสามารถของการช่วยการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="e2b84-112">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="e2b84-113">ภาพรวมเกี่ยวกับการปฏิบัติตามกฎระเบียบ</span><span class="sxs-lookup"><span data-stu-id="e2b84-113">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="e2b84-114">เพิ่มหน้านโยบายความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="e2b84-114">Add a privacy policy page</span></span>](add-privacy-page.md)
