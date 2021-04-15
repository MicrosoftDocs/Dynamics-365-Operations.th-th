---
title: ตั้งค่าคอนฟิกและกรองข้อมูลพื้นที่ทำงาน
description: บทความนี้แสดงภาพรวมเกี่ยวกับวิธีการตั้งค่าคอนฟิก และการกรองข้อมูลพื้นที่ทำงาน
author: jasongre
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankTreasurerWorkspace, HcmBenefitWorkspace, BudgetPlanningWorkspace, BusinessProcessGenericWorkspace, RetailCatalogManagementWorkspace, RetailCategoryAndProductWorkspace, RetailChannelManagementWorkspace, HcmCompensationWorkspace, CAMCostAccountingLedgerAdminWorkspace, CostAdminWorkspace, CostAnalysisWorkspace, CAMCostControlWorkspace, CustomerCollectionManagerWorkspace, CustomerInvoiceWorkspace, CustPaymentWorkspace, DataManagementWorkspace, DataValidationWorkspace, ERWorkspace, LedgerPeriodCloseProjectWorkspace, AssetWorkspace, GeneralJournalEntryWorkspace, VendVendorPortalInvoiceWorkspace, BudgetTrackingWorkspace, ReqCreatePlanWorkspace, BusinessProcessGenericOwnerWorkspace, SelfHealingWorkspace, WHSOutboundWorkMonitoringWorkspace, WHSWavePlanningWorkspace, PayrollWorkspace, HcmWorkforceWorkspace, RetailDiscountPricingWorkspace, EcoResProductDiscreteManufacturingWorkspace, KanbanPrepareProductForLeanWorkspace, EcoResProductProcessManufacturingWorkspace, EcoResProductVariantMaintainWorkspace, JmgShopSupervisorWorkspace, ProjProjectManagementWorkspace, VendVendorPortalWorkspace, PurchOrderMaintainWorkspace, PurchOrderProcessReceiptsWorkspace, HcmRecruitmentWorkspace, EcoResProductMaintainWorkspace, FMClerkWorkspace, OpResLifecycleManagementWorkspace, RetailITWorkspace, RetailChannelOperationsWorkspace, RetailStoreManagementWorkspace, SalesOrderProcessingWorkspace, SalesReturnWorkspace, SystemAdministrationWorkspaceForm, VendVendorRequestForQuotationsWorkspace, VendVendorProfileManagementWorkspace, VendInvoiceWorkspace, VendPaymentWorkspace
audience: Application User
ms.reviewer: sericks
ms.custom: 17491
ms.assetid: 541e6012-4680-4684-8494-e9b5ca4684ee
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d92427c1aeee92921b5b817b67530cf8aeddbbfb
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744038"
---
# <a name="configure-and-filter-workspaces"></a>ตั้งค่าคอนฟิกและกรองข้อมูลพื้นที่ทำงาน

[!include [banner](../includes/banner.md)]

บทความนี้แสดงภาพรวมเกี่ยวกับวิธีการตั้งค่าคอนฟิก และการกรองข้อมูลพื้นที่ทำงาน

## <a name="configuring-a-workspace"></a>การตั้งค่าคอนฟิกพื้นที่ทำงาน

คุณสามารถเปลี่ยนลักษณะและพฤติกรรมของบางพื้นที่ทำงาน ด้วยการปรับปรุงการตั้งค่าที่นำไปใช้กับพื้นที่ทำงานทั้งหมด เมื่อมีพื้นที่ทำงานที่คุณสามารถกำหนดค่า บานหน้าต่างการดำเนินการมีปุ่มที่แนะนำให้คุณคลิก เพื่อที่จะทำการเปลี่ยนแปลงการตั้งค่าคอนฟิก ตัวอย่างเช่น ในภาพประกอบต่อไปนี้ ปุ่มชื่อว่า **การตั้งค่าคอนฟิกพื้นที่ทำงานของฉัน**

[![ตั้งค่าคอนฟิกและกรองข้อมูลพื้นที่ทำงาน](./media/configure-and-filter-workspaces.png)](./media/configure-and-filter-workspaces.png)

เมื่อคุณคลิกปุ่ม กล่องโต้ตอบจะปรากฏขึ้น ซึ่งคุณสามารถปรับเปลี่ยนการตั้งค่าที่กำหนดไว้ล่วงหน้าสำหรับพื้นที่ทำงาน การตั้งค่าเฉพาะที่คุณเห็นในกล่องโต้ตอบนี้จะแตกต่างกันไปตามแต่ละพื้นที่ทำงาน และขึ้นอยู่กับการควบคุมเฉพาะและข้อมูลธุรกิจที่พร้อมใช้ในพื้นที่ทำงาน

[![ตั้งค่าคอนฟิกพื้นที่ทำงานของฉัน](./media/configure-my-workspace.png)](./media/configure-my-workspace.png)

## <a name="filtering-a-workspace"></a>การกรองข้อมูลพื้นที่ทำงาน

หลายพื้นที่ทำงานให้คุณกรองเนื้อหาที่ปรากฏในนั้น ตัวควบคุมที่มีอยู่อาจช่วยให้คุณสามารถกรองเนื้อหาทั้งหมดในพื้นที่ทำงานหรือเนื้อหาในส่วนเฉพาะของพื้นที่ทำงานเท่านั้น ตัวกรองบนพื้นที่ทำงานสามารถเป็นการค้นหา กล่องคำสั่งผสม ฟิลด์ข้อความอิสระ หรือตัวควบคุมชนิดอื่น อย่างไรก็ตาม ตัวกรองทุกชนิดมีผลกระทบเดียวกัน ตามที่อธิบายไว้ในส่วนต่อไปนี้

### <a name="workspace-wide-filters"></a>การกรองทั้งพื้นที่ทำงาน

คุณสามารถกรองพื้นที่ทำงานทั้งหมด โดยใช้ตัวกรองทั้งพื้นที่ทำงาน ตัวกรองทั้งพื้นที่ทำงานจะอยู่ในมุมบนซ้ายของพื้นที่ทำงาน เมื่อคุณเลือกค่าที่ระบุในรายการแบบหล่นลง เนื้อหาของพื้นที่ทำงานจะถูกกรองตามส่วนที่เลือก

[![ตัวกรองพื้นที่ทำงาน](./media/workspace-filter.png)](./media/workspace-filter.png)

เมื่อคุณคลิกเพื่อเปิดตัวกรอง ตัวเลือกต่างๆ จะถูกแสดง

[![ตัวกรองทั้งพื้นที่ทำงานแบบขยาย](./media/workspace-filter-expanded.png)](./media/workspace-filter-expanded.png)

เลือกตัวเลือกเพื่อกรองข้อมูลพื้นที่ทำงานตามตัวเลือกนั้น

### <a name="workspace-section-filters&quot;></a>ตัวกรองพื้นที่ทำงานตามส่วน

ถ้าแต่ละส่วนของพื้นที่ทำงานมีตัวกรอง คุณสามารถกรองข้อมูลแต่ละส่วนแยกต่างหาก ในภาพประกอบต่อไปนี้ ตัวกรอง (ฟิลด์ที่ประกอบด้วยข้อความ &quot;ตัวกรอง") เป็นตัวอย่างของตัวกรองในฟิลด์ข้อความอิสระ

[![ตัวกรองพื้นที่ทำงานตามส่วน](./media/workspace-section-filters.png)](./media/workspace-section-filters.png)

จากตัวกรองทั้งพื้นที่ทำงาน ให้เลือกหรือป้อนค่าตัวกรองที่ต้องการเพื่อจำกัดการแสดงเนื้อหาของส่วน


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]