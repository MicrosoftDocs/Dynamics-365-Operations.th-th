---
title: เปิดใช้งาน Power BI สำหรับการบัญชีสินค้าคงคลังส่วนกลาง
description: หัวข้อนี้อธิบายวิธีการเปิดใช้งาน Microsoft Power BI สำหรับการบัญชีสินค้าคงคลังส่วนกลาง
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d7979ed18b98ee6133774cd91bc866d6fca92d5f
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273233"
---
# <a name="enable-power-bi-for-global-inventory-accounting"></a><span data-ttu-id="04760-103">เปิดใช้งาน Power BI สำหรับการบัญชีสินค้าคงคลังส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="04760-103">Enable Power BI for Global Inventory Accounting</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="04760-104">คุณสามารถปักหมุดไทล์ แดชบอร์ด และรายงานจากบัญชี [PowerBI.com](https://powerbi.com/) ของคุณไปยังพื้นที่ทำงานแอปพลิเคชัน Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="04760-104">You can pin tiles, dashboards, and reports from your [PowerBI.com](https://powerbi.com/) account to your Microsoft Dynamics 365 application workspace.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="04760-105">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="04760-105">Prerequisites</span></span>

<span data-ttu-id="04760-106">ข้อเบื้องต้นต่อไปนี้ต้องอยู่ก่อนคุณจึงจะสามารถเปิดใช้งานการรายงาน Power BI ได้:</span><span class="sxs-lookup"><span data-stu-id="04760-106">The following prerequisites must be in place before you can enable Power BI reporting:</span></span>

- <span data-ttu-id="04760-107">คุณต้องเป็นผู้ดูแลระบบในแอปพลิเคชัน Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="04760-107">You must be a system administrator in the Dynamics 365 application.</span></span>
- <span data-ttu-id="04760-108">คุณต้องมีบัญชี [PowerBI.com](https://powerbi.com/)</span><span class="sxs-lookup"><span data-stu-id="04760-108">You must have a [PowerBI.com](https://powerbi.com/) account.</span></span>
- <span data-ttu-id="04760-109">คุณต้องมีอย่างน้อยหนึ่งแดชบอร์ดและหนึ่งรายงานในบัญชี Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="04760-109">You must have at least one dashboard and one report in your Power BI account.</span></span>
- <span data-ttu-id="04760-110">คุณต้องเป็นผู้ดูแลระบบของบัญชี Azure Active Directory (Azure AD) ของคุณ</span><span class="sxs-lookup"><span data-stu-id="04760-110">You must be an administrator for your Azure Active Directory (Azure AD) account.</span></span>
- <span data-ttu-id="04760-111">โดเมน Azure AD ต้องเป็นโดเมนเดียวกันกับที่คุณใช้บัญชี [PowerBI.com](https://powerbi.com/) ของคุณ</span><span class="sxs-lookup"><span data-stu-id="04760-111">The Azure AD domain must be the same domain that you used for your [PowerBI.com](https://powerbi.com/) account.</span></span>

## <a name="setup"></a><span data-ttu-id="04760-112">ตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="04760-112">Setup</span></span>

<span data-ttu-id="04760-113">หากต้องการตั้งค่าการรวม Power BI ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="04760-113">To set up the Power BI integration, follow these steps.</span></span>

1. <span data-ttu-id="04760-114">ลงชื่อเข้าใช้ [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index)</span><span class="sxs-lookup"><span data-stu-id="04760-114">Sign in to [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span></span>
1. <span data-ttu-id="04760-115">ไปที่ **ไลบรารีสินทรัพย์ที่ใช้ร่วมกัน** เลือก **แบบจำลองรายงาน Power BI** เป็นชนิดสินทรัพย์ และดาวน์โหลดแพคเกจ **การบัญชีสินค้าคงคลังส่วนกลาง**</span><span class="sxs-lookup"><span data-stu-id="04760-115">Go to **Shared asset library**, select **Power BI report model** as the asset type, and download the **Global Inventory Accounting** package.</span></span> 
1. <span data-ttu-id="04760-116">ลงชื่อเข้าใช้ [PowerBI.com](https://app.powerbi.com/) และอัปโหลดไฟล์รายงาน **การบัญชีสินค้าคงคลังส่วนกลาง** ของ Power BI ตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="04760-116">Sign in to [PowerBI.com](https://app.powerbi.com/), and upload the **Global Inventory Accounting** Power BI report file by following these steps:</span></span>

    1. <span data-ttu-id="04760-117">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="04760-117">Select **New**.</span></span>
    1. <span data-ttu-id="04760-118">เลือก **อัปโหลดไฟล์**</span><span class="sxs-lookup"><span data-stu-id="04760-118">Select **Upload a file**.</span></span>
    1. <span data-ttu-id="04760-119">เลือกไฟล์รายงาน **การบัญชีสินค้าคงคลังส่วนกลาง** ของ Power BI</span><span class="sxs-lookup"><span data-stu-id="04760-119">Select the **Global Inventory Accounting** Power BI report file.</span></span>

1. <span data-ttu-id="04760-120">ตั้งค่าคอนฟิกรายงาน **การบัญชีสินค้าคงคลังส่วนกลาง** ของ Power BI โดยปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="04760-120">Configure the **Global Inventory Accounting** Power BI report by following these steps:</span></span>

    1. <span data-ttu-id="04760-121">ไปที่ **พื้นที่ทำงานของฉัน** ค้นหาชุดข้อมูลของการบัญชีสินค้าคงคลังส่วนกลาง จากนั้นไปที่เมนู **ตัวเลือก** ให้เลือก **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="04760-121">Go to **My workspace**, find the dataset for Global Inventory Accounting, and then, on the **Options** menu, select **Settings**.</span></span>
    1. <span data-ttu-id="04760-122">ใน **การตั้งค่าการบัญชีสินค้าคงคลังส่วนกลาง** ให้ขยาย **พารามิเตอร์** และอัปเดตพารามิเตอร์ทั้งหมดตามที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="04760-122">In **Settings for Global inventory accounting**, expand **Parameters**, and update all parameters as required.</span></span>

1. <span data-ttu-id="04760-123">ลงทะเบียนแอปพลิเคชันตามที่อธิบายไว้ใน [ตั้งค่าคอนฟิกการรวม PowerBI.com](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process)</span><span class="sxs-lookup"><span data-stu-id="04760-123">Register the application as described in [Configure PowerBI.com integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process).</span></span>
1. <span data-ttu-id="04760-124">รวมไฟล์รายงาน **การบัญชีสินค้าคงคลังส่วนกลาง** ของ Power BI ลงใน Dynamics 365 Supply Chain Management โดยปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="04760-124">Integrate the **Global Inventory Accounting** Power BI report file into Dynamics 365 Supply Chain Management by following these steps:</span></span>

    1. <span data-ttu-id="04760-125">ไปที่ **การจัดการระบบ \> การตั้งค่า \> การตั้งค่าคอนฟิก PowerBI.com**</span><span class="sxs-lookup"><span data-stu-id="04760-125">Go to **System administration \> Setup \> PowerBI.com configuration**.</span></span>
    1. <span data-ttu-id="04760-126">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="04760-126">Select **Edit**.</span></span>
    1. <span data-ttu-id="04760-127">เลือก **เปิดใช้งานการรวม PowerBI.Com**</span><span class="sxs-lookup"><span data-stu-id="04760-127">Select **Enable PowerBI.Com integration**.</span></span>
    1. <span data-ttu-id="04760-128">ในฟิลด์ **รหัสแอพลิเคชัน** ให้ป้อนรหัสแอปพลิเคชัน:</span><span class="sxs-lookup"><span data-stu-id="04760-128">In the **Application ID** field, enter the application ID.</span></span>
    1. <span data-ttu-id="04760-129">ในฟิลด์ **คีย์แอพลิเคชัน** ให้ป้อนคีย์แอปพลิเคชัน:</span><span class="sxs-lookup"><span data-stu-id="04760-129">In the **Application key** field, enter the application key.</span></span>
    1. <span data-ttu-id="04760-130">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="04760-130">Select **Save**.</span></span>

1. <span data-ttu-id="04760-131">รีเฟรชหน้าเพื่อให้กล่องโต้ตอบการลงชื่อเข้าใช้ Power BI ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="04760-131">Refresh the page so that the Power BI sign-in dialog box appears.</span></span>
1. <span data-ttu-id="04760-132">บนแท็บ **ตัวเลือก** ให้เลือก **เปิดแค็ตตาล็อกรายงาน** แล้วเลือกไฟล์รายงาน **การบัญชีสินค้าคงคลังส่วนกลาง** ของ Power BI ที่คุณอัปโหลดไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="04760-132">On the **Options** tab, select **Open report catalog**, and then select the **Global Inventory Accounting** Power BI report file that you uploaded earlier.</span></span>
1. <span data-ttu-id="04760-133">รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="04760-133">Refresh the page.</span></span> <span data-ttu-id="04760-134">คุณควรดูว่ามีการเพิ่มรายงานแล้ว</span><span class="sxs-lookup"><span data-stu-id="04760-134">You should see that your report has been added.</span></span>
1. <span data-ttu-id="04760-135">ใต้ **รายงาน Power BI** เลือกลิงค์ **การบัญชีสินค้าคงคลังส่วนกลาง**</span><span class="sxs-lookup"><span data-stu-id="04760-135">Under **Power BI reports**, select the **Global Inventory Accounting** link.</span></span>

<span data-ttu-id="04760-136">สำหรับข้อมูลเพิ่มเติม ดู [ตั้งค่าคอนฟิกการรวม PowerBI.com](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md)</span><span class="sxs-lookup"><span data-stu-id="04760-136">For more information, see [Configure PowerBI.com integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).</span></span>
