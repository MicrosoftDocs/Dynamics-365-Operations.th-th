---
title: คุณลักษณะที่เอาออกหรือเลิกสนับสนุนใน Dynamics 365 Supply Chain Management
description: หัวข้อนี้อธิบายคุณลักษณะที่ถูกลบออก หรือที่ถูกวางแผนไว้ว่าจะลบใน Dynamics 365 Supply Chain Management
author: kamaybac
manager: AnnBe
ms.date: 04/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 7502cd16129431d41d152508fb3b49ff85a5a9f8
ms.sourcegitcommit: f1db998ecfccca660eb15cc2739b12c8463fa54d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/04/2020
ms.locfileid: "3331259"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a><span data-ttu-id="b1296-103">คุณลักษณะที่เอาออกหรือเลิกสนับสนุนใน Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b1296-103">Removed or deprecated features in Dynamics 365 Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1296-104">หัวข้อนี้จะได้รับการปรับปรุง เมื่อมีการจัดทำเอกสารคุณลักษณะที่เอาออกหรือเลิกสนับสนุนใหม่สำหรับ Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b1296-104">This topic will be updated as new removed or deprecated features are documented for Dynamics 365 Supply Chain Management.</span></span>

- <span data-ttu-id="b1296-105">คุณลักษณะที่ *ถูกลบ* จะไม่พร้อมใช้งานในผลิตภัณฑ์อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="b1296-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="b1296-106">คุณลักษณะที่ *ถูกยกเลิกการใช้* ไม่ได้อยู่ในการพัฒนาที่ใช้งานอยู่ และอาจถูกลบออกในการปรับปรุงในอนาคต</span><span class="sxs-lookup"><span data-stu-id="b1296-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="b1296-107">รายการนี้มีไว้เพื่อช่วยคุณพิจารณาการลบออกและการยกเลิกการใช้งานเหล่านี้สำหรับการวางแผนของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="b1296-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span>

> [!NOTE]
> <span data-ttu-id="b1296-108">ข้อมูลโดยละเอียดเกี่ยวกับออบเจ็กต์ต่างๆ ในแอป Finance and Operations พบได้ใน [รายงานอ้างอิงทางเทคนิค](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep)</span><span class="sxs-lookup"><span data-stu-id="b1296-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="b1296-109">คุณสามารถเปรียบเทียบเวอร์ชันต่างๆ ของรายงานเหล่านี้ เพื่อเรียนรู้เกี่ยวกับออบเจ็กต์ที่เปลี่ยนแปลงหรือถูกลบออกในแต่ละรุ่นของแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b1296-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a><span data-ttu-id="b1296-110">คุณลักษณะที่เอาออกหรือที่เลิกสนับสนุนในการนำออกใช้ Supply Chain Management 10.0.11</span><span class="sxs-lookup"><span data-stu-id="b1296-110">Features removed or deprecated in the Supply Chain Management 10.0.11 release</span></span>

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a><span data-ttu-id="b1296-111">การใช้กลไกจัดการการวางแผนหลักของ Supply Chain Management ในตัวสำหรับสถานการณ์จำลองการกระจาย</span><span class="sxs-lookup"><span data-stu-id="b1296-111">Use of built-in Supply Chain Management master planning engine for distribution scenarios</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b1296-112">**เหตุผลสำหรับการยกเลิกการใช้/การลบ**</span><span class="sxs-lookup"><span data-stu-id="b1296-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b1296-113">เมื่อต้องการปรับปรุงประสิทธิภาพการทำงานและลดการโหลดฐานข้อมูล SQL ในระหว่างการรันการวางแผนหลัก ระบบการวางแผนหลักของ Supply Chain Management ที่มีอยู่แล้วจะถูกแทนที่ด้วยการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="b1296-113">To enhance performance and minimize the SQL database load during master planning runs, the built-in Supply Chain Management master planning engine is being replaced by Planning Optimization.</span></span> <span data-ttu-id="b1296-114">การเพิ่มประสิทธิภาพการวางแผนช่วยให้สามารถทำงานได้อย่างรวดเร็ว ซึ่งสามารถดำเนินการได้แม้กระทั่งในเวลาทำการ</span><span class="sxs-lookup"><span data-stu-id="b1296-114">Planning Optimization allows for fast planning runs that can be performed even during office hours.</span></span> <span data-ttu-id="b1296-115">การทำเช่นนี้จะช่วยให้ผู้วางแผนสามารถตอบสนองต่อการเปลี่ยนแปลงในความต้องการหรือพารามิเตอร์การวางแผนได้ทันที</span><span class="sxs-lookup"><span data-stu-id="b1296-115">This enables planners to react immediately to changes in demand or planning parameters.</span></span> |
| <span data-ttu-id="b1296-116">**แทนที่ด้วยลักษณะการทำงานอื่นหรือไม่**</span><span class="sxs-lookup"><span data-stu-id="b1296-116">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b1296-117">ใช่ การเพิ่มประสิทธิภาพของการวางแผนจะแทนที่กลไกจัดการการวางแผนหลักของ Supply Chain Management ในตัวที่มีอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="b1296-117">Yes, Planning Optimization will replace the existing built-in Supply Chain Management master planning engine.</span></span> |
| <span data-ttu-id="b1296-118">**พื้นที่ของผลิตภัณฑ์ที่ได้รับผล**</span><span class="sxs-lookup"><span data-stu-id="b1296-118">**Product areas affected**</span></span>         | <span data-ttu-id="b1296-119">Supply Chain Management - การวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="b1296-119">Supply Chain Management - Master planning</span></span> |
| <span data-ttu-id="b1296-120">**ตัวเลือกการปรับใช้**</span><span class="sxs-lookup"><span data-stu-id="b1296-120">**Deployment option**</span></span>              | <span data-ttu-id="b1296-121">ระบบ Cloud เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="b1296-121">Cloud only.</span></span> <span data-ttu-id="b1296-122">การเพิ่มประสิทธิภาพการวางแผนไม่สนับสนุนการปรับใช้ในสถานที่</span><span class="sxs-lookup"><span data-stu-id="b1296-122">Planning Optimization is not supported with on-premises deployments.</span></span> |
| <span data-ttu-id="b1296-123">**สถานะ**</span><span class="sxs-lookup"><span data-stu-id="b1296-123">**Status**</span></span>                         | <span data-ttu-id="b1296-124">ยกเลิกการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="b1296-124">Deprecated.</span></span> <span data-ttu-id="b1296-125">ในเดือนเมษายน 2021 สถานการณ์จำลองการกระจายจะไม่ได้รับการสนับสนุนอีกต่อไปด้วยกลไกจัดการการวางแผนหลักของ Dynamics 365 Supply Chain Management ในตัว</span><span class="sxs-lookup"><span data-stu-id="b1296-125">On April 2021, distribution scenarios will no longer be supported with the built-in Dynamics 365 Supply Chain Management master planning engine.</span></span> <span data-ttu-id="b1296-126">สำหรับสถานการณ์จำลองการกระจาย ลูกค้าต้องใช้การเพิ่มประสิทธิภาพการวางแผนสำหรับการคำนวณการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="b1296-126">For distribution scenarios, customers must use Planning Optimization for master planning calculations.</span></span> <span data-ttu-id="b1296-127">สำหรับข้อมูลเพิ่มเติมให้ดูที่ [เอกสารประกอบการปรับการเพิ่มประสิทธิภาพการวางแผน](https://go.microsoft.com/fwlink/?linkid=2105830)</span><span class="sxs-lookup"><span data-stu-id="b1296-127">For more information, see [Planning Optimization documentation](https://go.microsoft.com/fwlink/?linkid=2105830).</span></span> <span data-ttu-id="b1296-128">ลูกค้าที่มีการปรับใช้ในสถานที่ของ Dynamics 365 Supply Chain Management อาจดำเนินการต่อไปเพื่อใช้กลไกจัดการการวางแผนหลักของ Supply Chain Management สำหรับสถานการณ์การกระจายหลังจากเดือนเมษายน 2021</span><span class="sxs-lookup"><span data-stu-id="b1296-128">Customers with on-premises deployments of Dynamics 365 Supply Chain Management may continue to use the Supply Chain Management master planning engine for distribution scenarios after April 2021.</span></span> <span data-ttu-id="b1296-129">อย่างไรก็ตาม จะไม่มีการปรับปรุงลักษณะการทำงานเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="b1296-129">However, no more feature enhancements will be provided.</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="b1296-130">ประกาศก่อนหน้านี้เกี่ยวกับคุณลักษณะที่ถูกลบหรือเลิกสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="b1296-130">Previous announcements about removed or deprecated features</span></span>

<span data-ttu-id="b1296-131">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับคุณลักษณะที่ถูกลบออกหรือเลิกสนับสนุนในรุ่นก่อนหน้านี้ ให้ดูที่ [คุณลักษณะที่ถูกลบออกหรือเลิกสนับสนุนในรุ่นก่อนหน้านี้](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md)</span><span class="sxs-lookup"><span data-stu-id="b1296-131">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span></span>
