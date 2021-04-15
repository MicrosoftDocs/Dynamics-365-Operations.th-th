---
title: ระบุตำแหน่งที่ตั้งของที่เก็บข้อมูลที่กำหนดเองสำหรับเอกสารที่จัดทำ
description: หัวข้อนี้อธิบายวิธีการขยายรายการของสถานที่เก็บสำหรับเอกสารที่รูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) สร้างขึ้น
author: NickSelin
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 25719de3d86785442e00f7375de525b95bdb094d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753707"
---
# <a name="specify-custom-storage-locations-for-generated-documents"></a>ระบุตำแหน่งที่ตั้งของที่เก็บข้อมูลที่กำหนดเองสำหรับเอกสารที่จัดทำ

[!include[banner](../includes/banner.md)]

Application Programming Interface (API) ของกรอบงานการรายงานทางอิเล็กทรอนิกส์ (ER) ช่วยให้คุณสามารถขยายรายการของสถานที่เก็บสำหรับเอกสารที่รูปแบบ ER สร้าง หัวข้อนี้จะอธิบายถึงวิธีการเพิ่มสถานที่เก็บที่กำหนดเองสำหรับเอกสารที่สร้างขึ้นโดยการมอบหมายงานของการสร้างปลายทาง ER ให้กับโรงงานปลายทางเริ่มต้นแล้วใช้คลาสที่กำหนดเองที่มีตรรกะปลายทางของตนเอง

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

ปรับใช้โทโพโลยีที่สนับสนุนการสร้างแบบต่อเนื่อง สำหรับข้อมูลเพิ่มเติม ดู [ปรับใช้โทโพโลยีซึ่งสนับสนุนการสร้างอย่างต่อเนื่องและระบบอัตโนมัติของการทดสอบ](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation) คุณต้องมีการเข้าถึงโทโพโลยีนี้สำหรับหนึ่งในบทบาทต่อไปนี้:

- นักพัฒนาการรายงานทางอิเล็กทรอนิกส์
- ที่ปรึกษาด้านการทำงานของการรายงานทางอิเล็กทรอนิกส์
- ผู้ดูแลระบบ

คุณต้องมีการเข้าถึงไปยังสภาพแวดล้อมการพัฒนาสำหรับโทโพโลยีนี้

คุณสามารถดำเนินงานทั้งหมดในหัวข้อนี้ให้เสร็จสมบูรณ์ได้ในบริษัท **USMF**

## <a name="import-the-fixed-asset-roll-forward-er-format"></a>นำเข้ารูปแบบ ER การกระทบยอดสินทรัพย์ถาวร

เมื่อต้องการสร้างเอกสารที่คุณต้องการเพิ่มที่ตั้งที่จัดเก็บแบบกำหนดเอง สำหรับ [การนำเข้า](er-download-configurations-global-repo.md) ตั้งค่าคอนฟิกรูปแบบ ER **การกระทบยอดสินทรัพย์ถาวร** ในโทโพโลยีปัจจุบัน

![หน้าที่เก็บการตั้งค่าคอนฟิก](./media/er-custom-storage-generated-files-import-format.png)

## <a name="run-the-fixed-asset-roll-forward-report"></a>เรียกใช้รายงานการกระทบยอดสินทรัพย์ถาวร

1. ไปที่ **สินทรัพย์ถาวร** \> **การสอบถามและรายงาน** \> **รายงานธุรกรรม** \> **การกระทบยอดสินทรัพย์ถาวร**
2. ในฟิลด์ **วันที่เริ่มต้น** ให้ป้อนวันที่ **1/1/2017** (มกราคม 1 2017)
3. ในฟิลด์ **วันที่นื้สิ้นสุด** ให้ป้อนวันที่ **1/31/2017** (มกราคม 31 2017)
4. ใน **ฟิลด์สกุลเงิน** ให้เลือก **สกุลเงินการบัญชี**
5. ในฟิลด์ **รูปแบบการแม็ป** ให้เลือก **การกระทบยอดสินทรัพย์ถาวร**
6. เลือก **ตกลง**

![กล่องโต้ตอบรันไทม์สำหรับรายงานการกระทบยอดสินทรัพย์ถาวร](./media/er-custom-storage-generated-files-runtime-dialog.png)

ใน Microsoft Excel ให้ตรวจสอบเอกสารขาออกที่สร้างขึ้นและพร้อมใช้งานสำหรับการดาวน์โหลด ลักษณะการทำงานนี้เป็น [ลักษณะการทำงานเริ่มต้น](electronic-reporting-destinations.md#default-behavior) สำหรับรูปแบบ ER ที่ไม่มีการตั้งค่าคอนฟิก [ปลายทาง](electronic-reporting-destinations.md) และที่กำลังทำงานในโหมดแบบโต้ตอบ

## <a name="review-the-source-code"></a>ตรวจสอบโค้ดต้นฉบับ

ทบทวนรหัสของวิธีการ `generateReportByGER()` ของคลาส `AssetRollForwardService` โปรดสังเกตว่า `Run()` มีการใช้วิธีการที่จะเรียกกรอบงาน ER และสร้างรายงาน **การกระทบยอดสินทรัพย์ถาวร**

```xpp
class AssetRollForwardService extends SysOperationServiceBase
{
    public const str ERFormatModelName = 'Fixed assets';
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'AssetRollForward';

    /// <summary>
    /// Generates report by general electronic reporting
    /// </summary>
    /// <param name = "_contract">The Asset Period Statement contract</param>
    public void generateReportByGER(AssetRollForwardContract _contract)
    {
        ERFormatMappingId   formatMappingId;
        AssetRollForwardDP  dataProvider;
        AssetRollForwardTmp assetRollForwardTmp;
        Query               query;

        query = new Query(SysOperationHelper::base64Decode(_contract.parmQuery()));
        dataProvider = AssetRollForwardDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        assetRollForwardTmp = dataProvider.getAssetRollForwardTmp(_contract, query);

        if (assetRollForwardTmp)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionDatabaseContext().addTemporaryTable(assetRollForwardTmp))
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, 'MyParameters', _contract, true));

                // Call ER to generate the report.
                ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName)
                    .withParameter(parameters)
                    .withFileDestination(_contract.getFileDestination())
                    .run();
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

## <a name="modify-the-source-code"></a>ปรับเปลี่ยนโค้ดต้นฉบับ

1. ในโครงการของคุณ Visual Studio ให้เพิ่มคลาสใหม่ (`AssetRollForwardDestination` ในตัวอย่างนี้) และเขียนรหัสเพื่อใช้ปลายทางที่กำหนดเองของคุณสำหรับรายงาน **การกระทบยอดสินทรัพย์ถาวร** ที่สร้างขึ้น

    - วิธีการ `new()` ได้รับการออกแบบมาเพื่อให้มีออบเจ็กต์ปลายทางของ ER ดั้งเดิมและพารามิเตอร์ที่ควบคุมโดยตรรกะของโปรแกรมประยุกต์ที่ระบุที่ตั้งที่กำหนดเองซึ่งควรจัดเก็บรายงานที่สร้างขึ้น ในตัวอย่างนี้ ที่ตั้งที่กำหนดเองคือชื่อของโฟลเดอร์ของระบบไฟล์ท้องถิ่นของเซิร์ฟเวอร์ที่รันบริการเซิร์ฟเวอร์โปรแกรมประยุกต์ออบเจ็กต์ (AOS)
    - วิธีการ `saveFile()` นี้ได้รับการออกแบบมาเพื่อบันทึกเอกสารที่สร้างขึ้นไปยังโฟลเดอร์ของระบบไฟล์ท้องถิ่นของเซิร์ฟเวอร์ที่รันบริการ AOS

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;

    /// <summary>
    /// Destination class for <c>AssetRollForwardDestinationFactory</c> that stores a generated report.
    /// </summary>
    public class AssetRollForwardDestination implements ERIFileDestination
    {
        private ERIFileDestination originDestination;
        private str TargetFolder;

        /// <summary>
        /// Creates a stream for new file.
        /// </summary>
        /// <param name = "_fileName">Name of a new file.</param>
        /// <returns>Stream for new file.</returns>
        public System.IO.Stream newFileStream(System.String _fileName)
        {
            return originDestination.newFileStream(_fileName);
        }

        /// <summary>
        /// Saves file in destination.
        /// </summary>
        /// <param name = "_stream">A stream to save.</param>
        /// <param name = "_fileName">A file name.</param>
        /// <returns>Saved stream.</returns>
        public System.IO.Stream saveFile(System.IO.Stream _stream, System.String _fileName)
        {
            _stream.Seek(0, System.IO.SeekOrigin::Begin);
            using (var localStream = System.IO.File::OpenWrite(TargetFolder + _fileName))
            {
                _stream.CopyTo(localStream);
            }
            return _stream;
        }

        /// <summary>
        /// Constructs destination for fixed asset roll forward report.
        /// </summary>
        /// <param name = "_originDestination">The original destination.</param>
        /// <param name = "_TargetFoder">The folder to store a report that's being created.</param>
        /// <returns>The fixed asset roll forward destination.</returns>
        public static AssetRollForwardDestination construct(ERIFileDestination _originDestination, str _TargetFoder)
        {
            return new AssetRollForwardDestination(_originDestination, _TargetFoder);
        }

        protected void new(ERIFileDestination _originDestination, str _TargetFoder)
        {
            originDestination = _originDestination;
            TargetFolder = _TargetFoder;
        }
    }
    ```

2. ในโครงการ Visual Studio ของคุณ ให้เพิ่มคลาสใหม่ (`AssetRollForwardDestinationFactory` ในตัวอย่างนี้) และรหัสเขียนเพื่อตั้งค่าโรงงานปลายทางที่กำหนดเองซึ่งมอบสิทธิ์ในการสร้างปลายทางให้กับโรงงานปลายทางเริ่มต้น และตัดปลายทางไฟล์ด้วยปลายทางของคุณเอง

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    using Microsoft.Dynamics365.LocalizationFramework.Format.FileGeneration;

    /// <summary>
    /// Destination factory for using <c>AssetRollForwardDestinationFactory</c>.
    /// </summary>
    public class AssetRollForwardDestinationFactory implements ERIFileDestinationFactory, ERIFileDestinationFactoryPostProcessor
    {
        private ERIFileDestinationFactory originDestinationFactory;
        private str TargetFolder;

        /// <summary>
        /// Creates file destination for print management.
        /// </summary>
        /// <param name = "_fileDestination">A default file destination.</param>
        /// <param name = "_identification">An identification strategy.</param>
        /// <param name = "_rootContext">A root context.</param>
        /// <param name = "_root">A root element.</param>
        /// <returns>A file destination.</returns>
        public ERIDataDrivenFileDestination createPrintMgmtDestination(
            ERIFileDestination _fileDestination,
            ERIObjectIdentificationStrategy _identification,
            ERTextFormatDataContext _rootContext,
            ERTextFormatIFileComponent _root)
        {
            ERIDataDrivenFileDestination dataDrivenDestination = originDestinationFactory.createPrintMgmtDestination(
                _fileDestination,
                _identification,
                _rootContext,
                _root);

            IFileDestinationHost fileDestinationHost = dataDrivenDestination as IFileDestinationHost;
            if (fileDestinationHost)
            {
                fileDestinationHost.FileDestination = AssetRollForwardDestination::construct(
                    fileDestinationHost.get_FileDestination(),
                    TargetFolder);
            }

            return dataDrivenDestination;
        }

        /// <summary>
        /// Constructs the fixed asset roll forward destination factory.
        /// </summary>
        /// <param name = "_originDestinationFactory">The original destination.</param>
        /// <param name = "_TargetFolder">The string containing a folder name that corresponds to the report, that's being created.</param>
        /// <returns>The destination factory for the fixed asset roll forward report.</returns>
        public static AssetRollForwardDestinationFactory construct(ERIFileDestinationFactory _originDestinationFactory, str _TargetFolder)
        {
            AssetRollForwardDestinationFactory destinationFactory = new AssetRollForwardDestinationFactory(_originDestinationFactory, _TargetFolder);

            ERIFileDestinationFactoryPostProcessorsHost factoryPostProcessing = ERCast::asObject(destinationFactory.originDestinationFactory) as ERIFileDestinationFactoryPostProcessorsHost;

            if (factoryPostProcessing)
            {
                factoryPostProcessing.addDestinationPostProcessor(destinationFactory);
            }
            return destinationFactory;
        }

        public ERIFileDestination processDestinationAfterCreation(ERIFileDestination _sourceDestination)
        {
            return AssetRollForwardDestination::construct(_sourceDestination, TargetFolder);
        }

        protected void new(ERIFileDestinationFactory _originDestinationFactory, str _TargetFolder)
        {
            originDestinationFactory = _originDestinationFactory;
            TargetFolder = _TargetFolder;
        }
    }
    ```

3. ปรับเปลี่ยนคลาส `AssetRollForwardService` ที่มีอยู่ และเขียนโค้ดเพื่อตั้งค่าโรงงานปลายทางที่กำหนดเองสำหรับผู้วิ่งรายงาน โปรดสังเกตว่าเมื่อมีการสร้างโรงงานปลายทางที่กำหนดเอง จะมีการส่งผ่านพารามิเตอร์ที่ใช้ในการควบคุมโปรแกรมประยุกต์ที่ระบุโฟลเดอร์เป้าหมาย เมื่อต้องการจัดเก็บไฟล์ที่สร้างขึ้นในลักษณะนี้

    > [!NOTE] 
    > ตรวจสอบให้แน่ใจว่าโฟลเดอร์ที่ระบุ (**c:\\0** ในตัวอย่างนี้) แสดงอยู่ในระบบไฟล์ท้องถิ่นของเซิร์ฟเวอร์ที่รันบริการ AOS มิฉะนั้น ข้อยกเว้น [DirectoryNotFoundException](https://docs.microsoft.com/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1) จะเกิดขึ้นในขณะรันไทม์

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    /// <summary>
    /// The electronic reporting service class for fixed asset roll forward report
    /// </summary>
    class AssetRollForwardService extends SysOperationServiceBase
    {
        public const str ERFormatModelName = 'Fixed assets';
        public const str ERModelDataSourceName = 'model';
        public const str DefaultExportedFileName = 'AssetRollForward';

        /// <summary>
        /// Generates report by general electronic reporting
        /// </summary>
        /// <param name = "_contract">The Asset Period Statement contract</param>
        public void generateReportByGER(AssetRollForwardContract _contract)
        {
            ERFormatMappingId   formatMappingId;
            AssetRollForwardDP  dataProvider;
            AssetRollForwardTmp assetRollForwardTmp;
            Query               query;

            query = new Query(SysOperationHelper::base64Decode(_contract.parmQuery()));
            dataProvider = AssetRollForwardDP::construct();
            formatMappingId = _contract.parmFormatMapping();
            assetRollForwardTmp = dataProvider.getAssetRollForwardTmp(_contract, query);

            if (assetRollForwardTmp)
            {
                try
                {
                    ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                        .add(new ERModelDefinitionDatabaseContext().addTemporaryTable(assetRollForwardTmp))
                        .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, 'MyParameters', _contract, true));

                    // Call ER to generate the report.
                    ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());

                    ERIFileDestinationFactoryHost factoryHost = ERCast::asObject(formatMappingRun) as ERIFileDestinationFactoryHost;
                    if (factoryHost)
                    {
                        ERIFileDestinationFactory fileDestinationFactory = factoryHost.getFileDestinationFactory();
                        factoryHost.setFileDestinationFactory(AssetRollForwardDestinationFactory::construct(fileDestinationFactory, @'c:\0\'));
                        formatMappingRun.run();
                    }
                }
                catch
                {
                    // An error occurred while exporting data.
                    error("@SYP4861341");
                }
            }
            else
            {
                // There is no data available.
                info("@SYS300117");
            }
        }
    }
    ```

4. สร้างโครงการของคุณใหม่

## <a name="re-run-the-fixed-asset-roll-forward-report"></a>เรียกใช้รายงานการกระทบยอดสินทรัพย์ถาวรอีกครั้ง

1. ไปที่ **สินทรัพย์ถาวร** \> **การสอบถามและรายงาน** \> **รายงานธุรกรรม** \> **การกระทบยอดสินทรัพย์ถาวร**
2. ในฟิลด์ **จากวันที่** ให้ป้อน **1/1/2017**
3. ในฟิลด์ **ถึงวันที่** ให้ป้อน **1/31/2017**
4. ใน **ฟิลด์สกุลเงิน** ให้เลือก **สกุลเงินการบัญชี**
5. ในฟิลด์ **รูปแบบการแม็ป** ให้เลือก **การกระทบยอดสินทรัพย์ถาวร**
6. เลือก **ตกลง**
7. เลือกดูโฟลเดอร์ **c:\\0** ท้องถิ่น เพื่อค้นหาไฟล์ที่สร้าง

> [!NOTE]
> เนื่องจาก `originDestination` ไม่มีการใช้ออบเจ็กต์ในออบเจ็กต์ `AssetRollForwardDestination` ในตัวอย่างนี้ การตั้งค่าคอนฟิกสำหรับ [ปลายทาง](electronic-reporting-destinations.md) รูปแบบ ER จะถูกละเว้นเมื่อรันไทม์

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

- [ปลายทางการรายงานทางอิเล็กทรอนิกส์ (ER)](electronic-reporting-destinations.md)
- [หน้าแรกของความสามารถในการเพิ่มฟังก์ชัน](../extensibility/extensibility-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]