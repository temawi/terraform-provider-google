---
# ----------------------------------------------------------------------------
#
#     ***     AUTO GENERATED CODE    ***    Type: MMv1     ***
#
# ----------------------------------------------------------------------------
#
#     This file is automatically generated by Magic Modules and manual
#     changes will be clobbered when the file is regenerated.
#
#     Please read more about how to change this file in
#     .github/CONTRIBUTING.md.
#
# ----------------------------------------------------------------------------
subcategory: "Document AI"
page_title: "Google: google_document_ai_processor"
description: |-
  The first-class citizen for Document AI.
---

# google\_document\_ai\_processor

The first-class citizen for Document AI. Each processor defines how to extract structural information from a document.


To get more information about Processor, see:

* [API documentation](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.processors)
* How-to Guides
    * [Official Documentation](https://cloud.google.com/document-ai/docs/overview)

<div class = "oics-button" style="float: right; margin: 0 0 -15px">
  <a href="https://console.cloud.google.com/cloudshell/open?cloudshell_git_repo=https%3A%2F%2Fgithub.com%2Fterraform-google-modules%2Fdocs-examples.git&cloudshell_working_dir=documentai_processor&cloudshell_image=gcr.io%2Fgraphite-cloud-shell-images%2Fterraform%3Alatest&open_in_editor=main.tf&cloudshell_print=.%2Fmotd&cloudshell_tutorial=.%2Ftutorial.md" target="_blank">
    <img alt="Open in Cloud Shell" src="//gstatic.com/cloudssh/images/open-btn.svg" style="max-height: 44px; margin: 32px auto; max-width: 100%;">
  </a>
</div>
## Example Usage - Documentai Processor


```hcl
resource "google_document_ai_processor" "processor" {
  location = "us"
  display_name = "test-processor"
  type = "OCR_PROCESSOR"
}
```

## Argument Reference

The following arguments are supported:


* `type` -
  (Required)
  The type of processor. For possible types see the [official list](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations/fetchProcessorTypes#google.cloud.documentai.v1.DocumentProcessorService.FetchProcessorTypes)

* `display_name` -
  (Required)
  The display name. Must be unique.

* `location` -
  (Required)
  The location of the resource.


- - -


* `kms_key_name` -
  (Optional)
  The KMS key used for encryption/decryption in CMEK scenarios. See https://cloud.google.com/security-key-management.

* `project` - (Optional) The ID of the project in which the resource belongs.
    If it is not provided, the provider project is used.


## Attributes Reference

In addition to the arguments listed above, the following computed attributes are exported:

* `id` - an identifier for the resource with format `projects/{{project}}/locations/{{location}}/processors/{{name}}`

* `name` -
  The resource name of the processor.


## Timeouts

This resource provides the following
[Timeouts](/docs/configuration/resources.html#timeouts) configuration options:

- `create` - Default is 20 minutes.
- `delete` - Default is 20 minutes.

## Import


Processor can be imported using any of these accepted formats:

```
$ terraform import google_document_ai_processor.default projects/{{project}}/locations/{{location}}/processors/{{name}}
$ terraform import google_document_ai_processor.default {{project}}/{{location}}/{{name}}
$ terraform import google_document_ai_processor.default {{location}}/{{name}}
```

## User Project Overrides

This resource supports [User Project Overrides](https://registry.terraform.io/providers/hashicorp/google/latest/docs/guides/provider_reference#user_project_override).
