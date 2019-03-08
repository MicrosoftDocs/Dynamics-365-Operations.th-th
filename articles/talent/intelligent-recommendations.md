---
title: คำแนะนำอัจฉริยะ
description: หัวข้อนี้อธิบายวิธีการใช้ machine learning เพื่อให้คำแนะนำสำหรับงานและผู้สมัครงาน
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c6225a311f5ba0b65b45092a1f626b9d6aff3f5e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "306429"
---
# <a name="intelligent-recommendations"></a><span data-ttu-id="58e9e-103">คำแนะนำอัจฉริยะ</span><span class="sxs-lookup"><span data-stu-id="58e9e-103">Intelligent recommendations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="58e9e-104">Machine learning สามารถช่วยให้ผู้สรรหาและผู้จัดการการจ้างงานระบุผู้สมัครที่ดีที่สุดสำหรับตำแหน่งงานอย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="58e9e-104">Machine learning can help recruiters and hiring managers quickly identify top candidates for a position.</span></span> <span data-ttu-id="58e9e-105">นอกจากนี้ ยังสามารถช่วยผู้ที่มีแนวโน้มจะเป็นลูกค้าในการค้นหาตำแหน่งที่เหมาะกับโพรไฟล์และความสนใจของพวกเขามากที่สุด</span><span class="sxs-lookup"><span data-stu-id="58e9e-105">It can also help prospects find the position that best suits their profile and interests.</span></span> <span data-ttu-id="58e9e-106">เมื่อมีใช้ลักษณะการทำงานเหล่านี้ และมีผลป้อนกลับให้ คำแนะนำจะพัฒนา</span><span class="sxs-lookup"><span data-stu-id="58e9e-106">As these features are used, and feedback is provided, recommendations will improve.</span></span>

> [!NOTE] 
> - <span data-ttu-id="58e9e-107">คุณลักษณะคำแนะนำอัจฉริยะพร้อมใช้งานเฉพาะกับ add-on การว่าจ้างที่ครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="58e9e-107">The intelligent recommendation features are available only with the Comprehensive hiring add-on.</span></span>
> - <span data-ttu-id="58e9e-108">เพื่อเปิดใช้งานลักษณะการทำงานผู้สมัครและคำแนะนำงาน ผู้ดูแลระบบต้องเปิดตัวเลือกการแสดงตัวอย่างสำหรับรายการเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="58e9e-108">To enable the candidate and job recommendation features, an admin must turn on the preview options for them.</span></span> <span data-ttu-id="58e9e-109">ในศูนย์การจัดการ บนแท็บ **การจัดการคุณลักษณะ** ตรวจสอบให้แน่ใจว่า ตัวเลือก **ลักษณะการทำงานการแสดงตัวอย่าง** ถูกตั้งค่าเป็น **เปิด**</span><span class="sxs-lookup"><span data-stu-id="58e9e-109">In the Admin center, on the **Feature management** tab, make sure that the **Preview features** option is set to **On**.</span></span> <span data-ttu-id="58e9e-110">จากนั้น ตรวจสอบให้แน่ใจว่า ตัวเลือก **คำแนะนำสำหรับผู้สมัคร** และ **คำแนะนำงาน** แต่ละรายการ ถูกกำหนดเป็น **เปิด**</span><span class="sxs-lookup"><span data-stu-id="58e9e-110">Then make sure that the individual **Candidate recommendation** and **Job recommendation** options are set to **On**.</span></span>

## <a name="candidate-recommendations"></a><span data-ttu-id="58e9e-111">คำแนะนำสำหรับผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="58e9e-111">Candidate recommendations</span></span>

<span data-ttu-id="58e9e-112">เนื่องจากการลงรายการบัญชีงานอาจดึงดูดผู้สมัครหลายร้อยราย จึงอาจเป็นเรื่องยากสำหรับผู้สรรหาและผู้จัดการที่ว่าจ้างในการค้นหาผู้สมัครที่มีทักษะและเบื้องหลังตรงกับตำแหน่งมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="58e9e-112">Because job postings might attract hundreds of applicants, it can be difficult for recruiters and hiring managers to find the candidates whose skills and background best match the position.</span></span> <span data-ttu-id="58e9e-113">โดยการวิเคราะห์ความสัมพันธ์ระหว่างคำอธิบายงานและความต้องการ และข้อมูลจากประวัติย่อของผู้สมัครและโพรไฟล์ machine learning สามารถใช้เพื่อสร้างคำแนะนำผู้สมัครได้</span><span class="sxs-lookup"><span data-stu-id="58e9e-113">By analyzing the correlation between the job description and requirements, and data from the candidates' resumes and profiles, machine learning can be used to produce candidate recommendations.</span></span> <span data-ttu-id="58e9e-114">คำแนะนำผู้สมัครสามารถช่วยให้ผู้สรรหาและผู้จัดการที่ว่าจ้างสามารถระบุ talent ที่ดีที่สุด และเลื่อนไปยังขั้นสัมภาษณ์เร็วขึ้น</span><span class="sxs-lookup"><span data-stu-id="58e9e-114">Candidate recommendations can help recruiters and hiring managers identify the top talent and move them to the interview stage faster.</span></span> <span data-ttu-id="58e9e-115">สำหรับงานใดๆ หากมีผู้สมัครมากกว่าสิบรายหรือผู้ที่มีแนวโน้มจะเป็นลูกค้าที่มีโพรไฟล์ทั้งหมด หรือประวัติย่อ ผู้สมัครหรือผู้ที่มีแนวโน้มจะเป็นลูกค้าที่ใกล้เคียงข้อกำหนดของงานมากที่สุดปรากฏขึ้นในส่วน **ผู้สมัครที่จะพิจารณา** บนหน้า **งาน**</span><span class="sxs-lookup"><span data-stu-id="58e9e-115">For any job, if there are more than ten candidates or prospects who have resumes or complete profiles, the candidates or prospects who most closely meet the job's requirements appear in the **Applicants to consider** section on the **Job** page.</span></span>

<span data-ttu-id="58e9e-116">สำหรับผู้สมัครที่แนะนำใดๆ คุณสามารถเลือก **ดูผู้สมัคร** บนบัตรผู้สมัคร เพื่อตรวจทานโพรไฟล์ของผู้สมัคร และดำเนินการในใบสมัครของเขาหรือเธอ</span><span class="sxs-lookup"><span data-stu-id="58e9e-116">For any recommended candidate, you can select **View candidate** on the candidate card to review the candidate's profile and take action on his or her application.</span></span> <span data-ttu-id="58e9e-117">คุณสามารถใช้ปุ่มจุดไข่ปลา (**...**) เพื่อเปิดโพรไฟล์ของผู้สมัครในแท็บใหม่ คุณยังสามารถใช้ปุ่มจุดไข่ปลาเพื่อให้ผลป้อนกลับเกี่ยวกับคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="58e9e-117">You can use the ellipsis button (**...**) to open the candidate's profile on a new tab. You can also use the ellipsis button to provide feedback about the recommendation.</span></span> <span data-ttu-id="58e9e-118">ด้วยวิธีนี้ คุณสามารถช่วยปรับกลไกจัดการคำแนะนำ และปรับปรุงคำแนะนำในอนาคต</span><span class="sxs-lookup"><span data-stu-id="58e9e-118">In this way, you help fine-tune the recommendation engine and improve future recommendations.</span></span> <span data-ttu-id="58e9e-119">คำแนะนำใดๆ ที่คุณไม่พอใจจะถูกเอาออกจากส่วน **ผู้สมัครที่จะพิจารณา** เมื่อคุณรีเฟรชหน้า **งาน**</span><span class="sxs-lookup"><span data-stu-id="58e9e-119">Any recommendations that you don't like are removed from the **Applicants to consider** section when you refresh the **Job** page.</span></span> <span data-ttu-id="58e9e-120">คุณสามารถใช้บัตรผลป้อนกลับเพื่อบ่งชี้ว่า เพราะเหตุใดคุณจึงไม่พบว่าคำแนะนำมีประโยชน์</span><span class="sxs-lookup"><span data-stu-id="58e9e-120">You can use the feedback card to indicate why you didn't find the recommendation useful.</span></span>

## <a name="job-recommendations"></a><span data-ttu-id="58e9e-121">คำแนะนำสำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="58e9e-121">Job recommendations</span></span> 

<span data-ttu-id="58e9e-122">เมื่อผู้ที่มีแนวโน้มจะเป็นพนักงานใช้ไซต์การทำงานกับงาน มีการแนะนำตำแหน่งที่เปิดอื่นๆ ที่องค์กร</span><span class="sxs-lookup"><span data-stu-id="58e9e-122">When a prospective employee uses the career site to apply to a job, other open positions at the organization are recommended.</span></span> <span data-ttu-id="58e9e-123">คำแนะนำเหล่านี้ขึ้นอยู่กับใบสมัครในอดีตของผู้ที่มีแนวโน้มจะเป็นลูกค้า และขึ้นอยู่กับประวัติย่อของเขาหรือเธอ หรือโพรไฟล์ของผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="58e9e-123">These recommendations are based on the prospect's past applications, and on his or her resume or candidate profile.</span></span> <span data-ttu-id="58e9e-124">ดังนั้น คำแนะนำเกี่ยวกับงานช่วยให้ผู้ที่มีแนวโน้มจะเป็นลูกค้าสามารถระบุงานที่เหมาะสมที่สุดสำหรับพวกเขาอย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="58e9e-124">Therefore, job recommendations help prospects quickly identify the jobs that are the best fit for them.</span></span> <span data-ttu-id="58e9e-125">คำแนะนำเกี่ยวกับงานจะให้แก่ผู้ที่มีแนวโน้มจะเป็นลูกค้า ถ้ามีการลงรายการบัญชีงานมากกว่าสิบงานบนไซต์การทำงาน</span><span class="sxs-lookup"><span data-stu-id="58e9e-125">Job recommendations are provided to prospects if more than ten jobs are posted on the career site.</span></span> <span data-ttu-id="58e9e-126">ผู้ที่มีแนวโน้มจะเป็นลูกค้าสามารถเปิดรายละเอียดของการลงรายการบัญชีงานได้จากบัตรคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="58e9e-126">Prospects can open the details of a job posting from the recommendation card.</span></span> <span data-ttu-id="58e9e-127">นอกจากนี้ พวกเขายังสามารถให้ผลป้อนกลับเกี่ยวกับคำแนะนำเพื่อช่วยปรับปรุงคำแนะนำในอนาคตได้</span><span class="sxs-lookup"><span data-stu-id="58e9e-127">They can also provide feedback about a recommendation to help improve future recommendations.</span></span>
