# iscsi-tools

This extension provides both iscsi-tools and multipath-tools for managing iSCSI connections and multipath devices.

## Components

- **open-iscsi**: Provides `iscsid` daemon and `iscsiadm` administration tool for iSCSI connections
- **multipath-tools**: Provides multipath utilities including `multipath`, `multipathd`, `multipathc`, `mpathpersist`, and `kpartx` for device mapper multipathing

## Usage

iscsi-tools has been tested with a remote iSCSI target with `iscsiadm` commands run in the mount namespace of the `ext-iscsid` Talos extension service.

For multipath support, use the multipath tools to manage redundant paths to storage devices. This is particularly useful for:
- HPE CSI driver deployments
- NetApp Trident ontap-san backend
- General external storage arrays requiring redundancy management
