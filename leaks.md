# BambuStudio 3MF metadata leaks

## `Metadata/model_settings.config` (XML)
- `config` > `object[]` > `part[]` > `metadata key=source_file`: 
  Includes a full path which may leak username.

## `Metadata/project_settings.config` (JSON)
- `version`:
  Leaks the application version.

## `Metadata/slice_info.config`
- `config` > `header` > `header_item key=X-BBL-Client-Version`:
  Leaks the application version.

## `3D/3dmodel.model` (XML)
- `model` > `metadata name=DesignerUserId`:
  Leaks the designer.
- `model` > `metadata name=Designer`:
  Leaks the designer.
- `model` > `metadata name=DesignerCover`:
  Leaks the designer.
- `model` > `metadata name=ModificationDate`:
  Leaks the timing.
- `model` > `metadata name=CreationDate`:
  Leaks the timing.
- `model` > `metadata name=Application`:
  Leaks the application version.
