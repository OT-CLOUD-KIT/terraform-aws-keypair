Keypair Moduel
______________

## Usage
_________________

```hcl

module "key_pair" {
  source                = "./KeyPair"
  create_key_pair       = var.create_key_pair
  create_private_key    = var.create_private_key
  private_key_algorithm = var.private_key_algorithm
  private_key_rsa_bits  = var.private_key_rsa_bits
  key_name              = var.key_name
  key_name_prefix       = var.key_name_prefix
  public_key            = var.public_key
  path                  = var.path
  s3_bucket_name        = var.s3_bucket_name
  s3_path               = var.s3_path
  tags                  = var.tags
}

```

## Variables
________________

```hcl


variable "create_private_key" {
  description = "enable private key creation"
  type = bool
  default = true
}

variable "private_key_algorithm" {
  description = "value"
  type = string
  default = "RSA"
}

variable "private_key_rsa_bits" {
  description = "value"
  type = number
  default = 4096
}

variable "create_key_pair" {
  description = "enable it to create key pair"
  type = bool
  default = true
}

variable "s3_bucket_name" {
  description = "The name for the s3 bucket to store key pair"
  type        = string
  default     = null
}

variable "key_name" {
  description = "The name for the key pair"
  type        = string
  default     = null
}

variable "key_name_prefix" {
  description = "Creates a unique name beginning with the specified prefix."
  type        = string
  default     = null
}

variable "public_key" {
  description = "The public key for existing public key"
  type        = string
  default     = ""
}

variable "path" {
  description = "value"
  type = string
  default = "."
}

variable "s3_path" {
  description = "value"
  type = string
  default = "."
}

variable "tags" {
  description = "tags for key-pair"
  type = map(string)
  default = { }
}

```
