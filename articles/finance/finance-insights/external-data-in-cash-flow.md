---
title: ใช้ข้อมูลภายนอกในการคาดการณ์กระแสเงินสด (ตัวอย่าง)
description: หัวข้อนี้จะอธิบายขั้นตอนการตั้งค่าที่คุณต้องดำเนินการให้เสร็จสมบูรณ์เพื่อให้สามารถป้อนหรือนำเข้าข้อมูลภายนอกเข้าในการคาดการณ์กระแสเงินสดได้
author: rcarlson
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 7d5768a6cb2b3623333fab93a42ac5840e87ec68
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818637"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a><span data-ttu-id="81dab-103">ใช้ข้อมูลภายนอกในการคาดการณ์กระแสเงินสด (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="81dab-103">Use external data in cash flow forecasts (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="81dab-104">คุณสามารถป้อนหรือนำเข้าข้อมูลภายนอกเข้าในการคาดการณ์กระแสเงินสดได้</span><span class="sxs-lookup"><span data-stu-id="81dab-104">External data can be entered or imported into cash flow forecasts.</span></span> <span data-ttu-id="81dab-105">หัวข้อนี้จะอธิบายขั้นตอนการตั้งค่าที่เกี่ยวข้องกับการใช้ข้อมูลภายนอกโดยเฉพาะและเปิดใช้งานข้อมูลภายนอกที่จะรวมไว้ในการคาดการณ์กระแสเงินสด</span><span class="sxs-lookup"><span data-stu-id="81dab-105">This topic describes the setup steps that are specific to the use of external data and that enable the external data to be included in a cash flow forecast.</span></span>

## <a name="external-data-setup"></a><span data-ttu-id="81dab-106">การตั้งค่าข้อมูลจากภายนอก</span><span class="sxs-lookup"><span data-stu-id="81dab-106">External data setup</span></span>

<span data-ttu-id="81dab-107">ใช้แท็บ **แหล่งที่มาภายนอก** ในหน้า **การตั้งค่าการคาดการณ์กระแสเงินสด** (**การจัดการเงินสดและธนาคาร \> การคาดการณ์กระแสเงินสด**) เพื่อป้อนการตั้งค่าที่สนับสนุนการใช้ข้อมูลภายนอกในการคาดการณ์กระแสเงินสด</span><span class="sxs-lookup"><span data-stu-id="81dab-107">Use the **External source** tab on the **Cash flow forecast setup** page (**Cash and bank management \> Cash flow forecasting**) to enter settings that support the use of external data in cash flow forecasts.</span></span>

<span data-ttu-id="81dab-108">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการตั้งค่า ให้ดูที่ [การคาดการณ์กระแสเงินสด](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting)</span><span class="sxs-lookup"><span data-stu-id="81dab-108">For more information about the setup, see [Cash flow forecasting](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting).</span></span>

<span data-ttu-id="81dab-109">เมื่อต้องการป้อนข้อมูลภายนอกสำหรับการคาดการณ์กระแสเงินสด คุณสามารถใช้ประสบการณ์เปิดใน Excel สำหรับการป้อนและการปรับเปลี่ยนข้อมูลภายนอก</span><span class="sxs-lookup"><span data-stu-id="81dab-109">To enter external data for cash flow forecasts, you can use the Open in Excel experience for entering and modifying external data.</span></span> <span data-ttu-id="81dab-110">เลือกปุ่ม **ข้อมูลภายนอก** แล้วเลือก **เพิ่มข้อมูลภายนอก** หรือ **แก้ไขข้อมูลภายนอกที่มีอยู่**</span><span class="sxs-lookup"><span data-stu-id="81dab-110">Select the **External data** button, and then select either **Add External Data** or **Edit existing external data**.</span></span> <span data-ttu-id="81dab-111">เมื่อ Microsoft Excel เปิดไฟล์แล้ว คุณสามารถป้อนข้อมูลในฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="81dab-111">When the Microsoft Excel file is opened, you can enter information in the following fields:</span></span>

- <span data-ttu-id="81dab-112">**รหัสรายการ**</span><span class="sxs-lookup"><span data-stu-id="81dab-112">**Entry ID**</span></span>
- <span data-ttu-id="81dab-113">**คำอธิบาย** (ไม่จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="81dab-113">**Description** (optional)</span></span>
- <span data-ttu-id="81dab-114">**ชื่อแหล่งที่มาภายนอก** – เลือกค่าใดค่าหนึ่งในรายการที่คุณได้กำหนดไว้เมื่อคุณตั้งค่าข้อมูลเชิงลึกทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="81dab-114">**External Source name** – Select one of the values in the list that you defined when you set up Finance Insights.</span></span>
- <span data-ttu-id="81dab-115">**นิติบุคคล**</span><span class="sxs-lookup"><span data-stu-id="81dab-115">**Legal Entity**</span></span>
- <span data-ttu-id="81dab-116">**วัน เดือน**</span><span class="sxs-lookup"><span data-stu-id="81dab-116">**Date**</span></span>
- <span data-ttu-id="81dab-117">**จำนวนเงินในสกุลเงินของธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="81dab-117">**Amount in transaction currency**</span></span>
- <span data-ttu-id="81dab-118">**รหัสสกุลเงิน**</span><span class="sxs-lookup"><span data-stu-id="81dab-118">**Currency Code**</span></span>
- <span data-ttu-id="81dab-119">**มิติเริ่มต้น** (ไม่จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="81dab-119">**Default Dimension** (optional)</span></span>
- <span data-ttu-id="81dab-120">**หมายเลขเอกสาร** (ไม่จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="81dab-120">**Document number** (optional)</span></span>
- <span data-ttu-id="81dab-121">**หมายเลขบัญชี** (ไม่จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="81dab-121">**Account number** (optional)</span></span>
- <span data-ttu-id="81dab-122">**ชื่อบัญชี** (ไม่จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="81dab-122">**Account name** (optional)</span></span>

## <a name="importing-external-data-by-using-the-data-management-framework"></a><span data-ttu-id="81dab-123">การนำเข้าข้อมูลภายนอกโดยใช้กรอบงานการจัดการข้อมูล</span><span class="sxs-lookup"><span data-stu-id="81dab-123">Importing external data by using the Data Management framework</span></span>

<span data-ttu-id="81dab-124">คุณสามารถนำเข้าข้อมูลภายนอกสำหรับการคาดการณ์กระแสเงินสดโดยใช้พื้นที่ทำงาน **การจัดการข้อมูล** และเอนทิตีที่มีการตั้งชื่อ **การคาดการณ์กระแสเงินสดสำหรับการคาดการณ์กระแสเงินสด**</span><span class="sxs-lookup"><span data-stu-id="81dab-124">You can import external data for cash flow forecasts by using the **Data Management** workspace and the entity that is named **Cash flow forecast external source entry**.</span></span>

<span data-ttu-id="81dab-125">นอกจากนี้ ถ้าคุณต้องการย้ายข้อมูลการตั้งค่าจากสภาพแวดล้อมหนึ่งไปยังอีกพื้นที่หนึ่ง เอนทิตีที่พร้อมใช้งานสำหรับตารางการตั้งค่าที่จำเป็นต้องใช้:</span><span class="sxs-lookup"><span data-stu-id="81dab-125">Additionally, if you must move setup data from one environment to another, the following entities area available for the setup tables that are required:</span></span>

- <span data-ttu-id="81dab-126">การตั้งค่าแหล่งที่มาภายนอกของการคาดการณ์กระแสเงินสด</span><span class="sxs-lookup"><span data-stu-id="81dab-126">Cash flow forecast external source setup</span></span>
- <span data-ttu-id="81dab-127">การตั้งค่านิติบุคคลที่เป็นแหล่งที่มาภายนอกของการคาดการณ์กระแสเงินสด</span><span class="sxs-lookup"><span data-stu-id="81dab-127">Cash flow forecast external source legal entity setup</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="81dab-128">ประกาศความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="81dab-128">Privacy notice</span></span>
<span data-ttu-id="81dab-129">การแสดงตัวอย่าง (1) อาจใช้วิธีการที่มีความปลอดภัยและความเป็นส่วนตัวที่น้อยลงกว่าบริการ Dynamics 365 Finance and Operations (2) ไม่ถูกรวมอยู่ในข้อตกลงระดับการให้บริการ (SLA) สำหรับบริการนี้ (3) ไม่ควรถูกใช้เพื่อประมวลผลข้อมูลส่วนบุคคลหรือข้อมูลอื่นที่อยู่ภายใต้ข้อกำหนดการปฏิบัติตามกฎหมายหรือระเบียบข้อบังคับ และ (4) มีการสนับสนุนที่จำกัด</span><span class="sxs-lookup"><span data-stu-id="81dab-129">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]