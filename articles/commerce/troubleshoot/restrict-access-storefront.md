---
title: จํากัดการเข้าถึงหน้าร้านในระหว่างการทดสอบหรือการพัฒนา
description: หัวข้อนี้อธิบายวิธีการจํากัดการเข้าถึงหน้าร้าน Microsoft Dynamics 365 Commerce ในขณะที่ทำการทดสอบภายในหรือการพัฒนา
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: cdc9b6af55bcba98f5ea7607bb1847f61a707778
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018349"
---
# <a name="restrict-access-to-a-storefront-during-testing-or-development"></a><span data-ttu-id="514b5-103">จํากัดการเข้าถึงหน้าร้านในระหว่างการทดสอบหรือการพัฒนา</span><span class="sxs-lookup"><span data-stu-id="514b5-103">Restrict access to a storefront during testing or development</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="514b5-104">หัวข้อนี้อธิบายวิธีการจํากัดการเข้าถึงหน้าร้าน Microsoft Dynamics 365 Commerce ในขณะที่ทำการทดสอบภายในหรือการพัฒนา</span><span class="sxs-lookup"><span data-stu-id="514b5-104">This topic explains how to restrict access to a Microsoft Dynamics 365 Commerce storefront while internal testing or development is occurring.</span></span>

## <a name="description"></a><span data-ttu-id="514b5-105">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="514b5-105">Description</span></span>

<span data-ttu-id="514b5-106">ในระหว่างทำการทดสอบภายในหรือการพัฒนา คุณอาจต้องการจํากัดการเข้าถึงไซต์ของคุณ เพื่อป้องกันไม่ให้ผู้ใช้ภายนอกเข้าถึงหน้าของหน้าร้านที่เผยแพร่อยู่ได้</span><span class="sxs-lookup"><span data-stu-id="514b5-106">During internal testing or active development, you might want to restrict access to your site to prevent external users from accessing the published storefront pages.</span></span>

## <a name="resolution"></a><span data-ttu-id="514b5-107">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="514b5-107">Resolution</span></span>

### <a name="set-up-azure-ad-b2c-by-using-standard-user-flows"></a><span data-ttu-id="514b5-108">ตั้งค่า Azure AD B2C โดยใช้โฟลว์ผู้ใช้มาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="514b5-108">Set up Azure AD B2C by using standard user flows</span></span>

<span data-ttu-id="514b5-109">หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับวิธีตั้งค่าคอนฟิก Azure Active Directory B2C (Azure AD B2C) ให้กับไซต์ e-commerce ของคุณ โปรดดูที่ [ตั้งค่าผู้เช่า B2C ใน Commerce](../set-up-b2c-tenant.md)</span><span class="sxs-lookup"><span data-stu-id="514b5-109">For information about how to configure Azure Active Directory B2C (Azure AD B2C) for your e-commerce site, see [Set up a B2C tenant in Commerce](../set-up-b2c-tenant.md).</span></span>

### <a name="restrict-user-access-to-storefront-pages-and-block-the-creation-of-new-users"></a><span data-ttu-id="514b5-110">จํากัดการเข้าถึงหน้าของหน้าร้านของผู้ใช้และบล็อคการสร้างผู้ใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="514b5-110">Restrict user access to storefront pages and block the creation of new users</span></span>

<span data-ttu-id="514b5-111">หากต้องการจํากัดการเข้าถึงหน้าของหน้าร้านของผู้ใช้โปรแกรมสร้างไซต์ Commerce ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="514b5-111">To restrict user access to storefront pages in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="514b5-112">ไปที่ไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="514b5-112">Go to your site.</span></span>
1. <span data-ttu-id="514b5-113">เลือก **หน้า** แล้วเลือกหน้าที่จะจํากัดการเข้าถึงของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="514b5-113">Select **Pages**, and then select the page to restrict user access for.</span></span>
1. <span data-ttu-id="514b5-114">เลือกโมดูลหรือช่องส่วนย่อย แล้วเลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="514b5-114">Select the module or fragment slot, and then select **Edit**.</span></span>
1. <span data-ttu-id="514b5-115">ในบานหน้าต่างคุณสมบัติ ให้เลือก **ต้องลงชื่อเข้าใช้หรือไม่** แล้วเลือก **เสร็จสิ้นการแก้ไข**</span><span class="sxs-lookup"><span data-stu-id="514b5-115">In the properties pane, select **Requires sign-in?**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="514b5-116">เลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="514b5-116">Select **Publish**.</span></span>

<span data-ttu-id="514b5-117">เมื่อต้องการบล็อคการสร้างผู้ใช้ใหม่ใน Azure AD ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="514b5-117">To block the creation of new users in Azure AD, follow these steps.</span></span>

1. <span data-ttu-id="514b5-118">ไปที่ [พอร์ทัล Azure](https://portal.azure.com/)</span><span class="sxs-lookup"><span data-stu-id="514b5-118">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="514b5-119">เลือกแอปพลิเคชัน Azure AD B2C ที่คุณสร้างขึ้นเพื่อการเข้าถึงไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="514b5-119">Select the Azure AD B2C application that you created for your site access.</span></span>
1. <span data-ttu-id="514b5-120">ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **โฟลว์ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="514b5-120">In the left navigation, select **User flows**.</span></span>
1. <span data-ttu-id="514b5-121">ที่ด้านบนของหน้า **โฟลว์ผู้ใช้** เลือก **โฟลว์ผู้ใช้ใหม่**</span><span class="sxs-lookup"><span data-stu-id="514b5-121">At the top of the **User Flows** page, select **New user flow**.</span></span>
1. <span data-ttu-id="514b5-122">บนหน้า **เลือกชนิดโฟลว์ผู้ใช้** ให้เลือก **แสดงตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="514b5-122">On the **Select a user flow type** page, select **Preview**.</span></span>
1. <span data-ttu-id="514b5-123">ตรงกลางของหน้า ให้เลือก **ลงชื่อเข้าใช้ v2**</span><span class="sxs-lookup"><span data-stu-id="514b5-123">In the middle of the page, select **Sign in v2**.</span></span> <span data-ttu-id="514b5-124">จากนั้นให้ปฏิบัติตามขั้นตอนใน [การตั้งค่าผู้เช่า B2C ใน Commerce](../set-up-b2c-tenant.md) เพื่อตั้งค่าคอนฟิกโฟลว์ตามโฟลว์มาตรฐานของผู้ใช้ Azure AD  B2C ของไซต์ของคุณในระหว่างการทดสอบหรือการพัฒนา</span><span class="sxs-lookup"><span data-stu-id="514b5-124">Then follow the steps in [Set up a B2C tenant in Commerce](../set-up-b2c-tenant.md) to configure the flow as your site's standard user flow for Azure AD B2C during testing or development.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="514b5-125">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="514b5-125">Additional resources</span></span>

[<span data-ttu-id="514b5-126">ตั้งค่าผู้เช่า B2C ใน Commerce</span><span class="sxs-lookup"><span data-stu-id="514b5-126">Set up a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)

[<span data-ttu-id="514b5-127">ตั้งค่าหน้าแบบกำหนดเองสำหรับการลงชื่อเข้าใช้ของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="514b5-127">Set up custom pages for user sign-ins</span></span>](../custom-pages-user-logins.md)
