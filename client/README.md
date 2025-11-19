# Cloudmersive.APIClient.NETCore.DocumentAI - the C# library for the Document AI API

Use next-generation AI to extract data, fields, insights and text from documents. Instantly.

This C# SDK is for the [Cloudmersive Document AI API](https://www.cloudmersive.com/document-ai-api):

- API version: v1
- SDK version: 1.0.8
- Build package: io.swagger.codegen.languages.CSharpClientCodegen

<a name="frameworks-supported"></a>
## Frameworks supported
- .NET Core >=1.0
- .NET Framework >=4.6
- Mono/Xamarin >=vNext
- UWP >=10.0

<a name="dependencies"></a>
## Dependencies
- FubarCoder.RestSharp.Portable.Core >=4.0.7
- FubarCoder.RestSharp.Portable.HttpClient >=4.0.7
- Newtonsoft.Json >=10.0.3

<a name="installation"></a>
## Installation
Generate the DLL using your preferred tool

Then include the DLL (under the `bin` folder) in the C# project, and use the namespaces:
```csharp
using Cloudmersive.APIClient.NETCore.DocumentAI.Api;
using Cloudmersive.APIClient.NETCore.DocumentAI.Client;
using Cloudmersive.APIClient.NETCore.DocumentAI.Model;
```
<a name="getting-started"></a>
## Getting Started

```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.DocumentAI.Api;
using Cloudmersive.APIClient.NETCore.DocumentAI.Client;
using Cloudmersive.APIClient.NETCore.DocumentAI.Model;

namespace Example
{
    public class Example
    {
        public void main()
        {

            // Configure API key authorization: Apikey
            Configuration.Default.ApiKey.Add("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.ApiKeyPrefix.Add("Apikey", "Bearer");

            var apiInstance = new AnalyzeApi();
            var body = new DocumentPolicyRequest(); // DocumentPolicyRequest | Input request, including document and policy rules (optional) 

            try
            {
                // Enforce Policies to a Document to allow or block it using Advanced AI
                DocumentPolicyResult result = apiInstance.ApplyRules(body);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling AnalyzeApi.ApplyRules: " + e.Message );
            }

        }
    }
}
```

<a name="documentation-for-api-endpoints"></a>
## Documentation for API Endpoints

All URIs are relative to *https://localhost*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AnalyzeApi* | [**ApplyRules**](docs/AnalyzeApi.md#applyrules) | **POST** /document-ai/document/analyze/enforce-policy | Enforce Policies to a Document to allow or block it using Advanced AI
*ExtractApi* | [**ExtractAllFieldsAndTables**](docs/ExtractApi.md#extractallfieldsandtables) | **POST** /document-ai/document/extract/all | Extract All Fields and Tables of Data from a Document using AI
*ExtractApi* | [**ExtractBarcodes**](docs/ExtractApi.md#extractbarcodes) | **POST** /document-ai/document/extract/barcodes | Extract Barcodes of from a Document using AI
*ExtractApi* | [**ExtractClassification**](docs/ExtractApi.md#extractclassification) | **POST** /document-ai/document/extract/classify | Extract Classification or Category from a Document using AI
*ExtractApi* | [**ExtractClassificationAdvanced**](docs/ExtractApi.md#extractclassificationadvanced) | **POST** /document-ai/document/extract/classify/advanced | Extract Classification or Category from a Document using Advanced AI
*ExtractApi* | [**ExtractFields**](docs/ExtractApi.md#extractfields) | **POST** /document-ai/document/extract/fields | Extract Field Values from a Document using AI
*ExtractApi* | [**ExtractFieldsAdvanced**](docs/ExtractApi.md#extractfieldsadvanced) | **POST** /document-ai/document/extract/fields/advanced | Extract Field Values from a Document using Advanced AI
*ExtractApi* | [**ExtractSummary**](docs/ExtractApi.md#extractsummary) | **POST** /document-ai/document/extract/summary | Extract Summary from a Document using AI
*ExtractApi* | [**ExtractTables**](docs/ExtractApi.md#extracttables) | **POST** /document-ai/document/extract/tables | Extract Tables of Data from a Document using AI
*ExtractApi* | [**ExtractText**](docs/ExtractApi.md#extracttext) | **POST** /document-ai/document/extract/text | Extract Text from a Document using AI
*RunBatchJobApi* | [**ExtractAllFieldsAndTablesFromDocumentBatchJob**](docs/RunBatchJobApi.md#extractallfieldsandtablesfromdocumentbatchjob) | **POST** /document-ai/document/batch-job/extract/all | Extract All Fields and Tables of Data from a Document using AI as a Batch Job
*RunBatchJobApi* | [**ExtractClassificationFromDocumentBatchJob**](docs/RunBatchJobApi.md#extractclassificationfromdocumentbatchjob) | **POST** /document-ai/document/batch-job/extract/classify | Extract Classification or Category from a Document using AI as a Batch Job
*RunBatchJobApi* | [**ExtractFieldsFromDocumentAdvancedBatchJob**](docs/RunBatchJobApi.md#extractfieldsfromdocumentadvancedbatchjob) | **POST** /document-ai/document/batch-job/extract/fields/advanced | Extract Field Values from a Document using Advanced AI as a Batch Job
*RunBatchJobApi* | [**ExtractTextFromDocumentBatchJob**](docs/RunBatchJobApi.md#extracttextfromdocumentbatchjob) | **POST** /document-ai/document/batch-job/extract/text | Extract Text from a Document using AI as a Batch Job
*RunBatchJobApi* | [**GetAsyncJobStatus**](docs/RunBatchJobApi.md#getasyncjobstatus) | **GET** /document-ai/document/batch-job/batch-job/status | Get the status and result of an Extract Document Batch Job


<a name="documentation-for-models"></a>
## Documentation for Models

 - [Model.AdvancedExtractClassificationRequest](docs/AdvancedExtractClassificationRequest.md)
 - [Model.AdvancedExtractFieldsRequest](docs/AdvancedExtractFieldsRequest.md)
 - [Model.DocumentAdvancedClassificationResult](docs/DocumentAdvancedClassificationResult.md)
 - [Model.DocumentCategories](docs/DocumentCategories.md)
 - [Model.DocumentClassificationResult](docs/DocumentClassificationResult.md)
 - [Model.DocumentPolicyRequest](docs/DocumentPolicyRequest.md)
 - [Model.DocumentPolicyResult](docs/DocumentPolicyResult.md)
 - [Model.ExtractBarcodesAiResponse](docs/ExtractBarcodesAiResponse.md)
 - [Model.ExtractDocumentBatchJobResult](docs/ExtractDocumentBatchJobResult.md)
 - [Model.ExtractDocumentJobStatusResult](docs/ExtractDocumentJobStatusResult.md)
 - [Model.ExtractFieldsAdvancedResponse](docs/ExtractFieldsAdvancedResponse.md)
 - [Model.ExtractFieldsAndTablesResponse](docs/ExtractFieldsAndTablesResponse.md)
 - [Model.ExtractFieldsResponse](docs/ExtractFieldsResponse.md)
 - [Model.ExtractTablesResponse](docs/ExtractTablesResponse.md)
 - [Model.ExtractTextResponse](docs/ExtractTextResponse.md)
 - [Model.ExtractedBarcodeItem](docs/ExtractedBarcodeItem.md)
 - [Model.ExtractedTextPage](docs/ExtractedTextPage.md)
 - [Model.FieldAdvancedValue](docs/FieldAdvancedValue.md)
 - [Model.FieldToExtract](docs/FieldToExtract.md)
 - [Model.FieldValue](docs/FieldValue.md)
 - [Model.PolicyRule](docs/PolicyRule.md)
 - [Model.PolicyRuleViolation](docs/PolicyRuleViolation.md)
 - [Model.SummarizeDocumentResponse](docs/SummarizeDocumentResponse.md)
 - [Model.TableResult](docs/TableResult.md)
 - [Model.TableResultCell](docs/TableResultCell.md)
 - [Model.TableResultRow](docs/TableResultRow.md)


<a name="documentation-for-authorization"></a>
## Documentation for Authorization

<a name="Apikey"></a>
### Apikey

- **Type**: API key
- **API key parameter name**: Apikey
- **Location**: HTTP header

