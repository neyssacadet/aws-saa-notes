# Object Versioning & MFA Delete

## Object Versioning

A bucket’s versioning starts off as disabled. It can then be enabled.
Once it is enabled it can be suspended and then re-enabled.
However, once a bucket’s versioning has been enabled, it can never be disabled again.

Object versioning allows us to store multiple versions of objects within a bucket.

Operations that modify objects generate a new version.

The way this works is that when versioning is disabled objects are only identifiable by the key which is actually their name.
The ID of these objects is set to null. (when versioning is disabled) 
When versioning is enabled, each object is assigned an ID.
New versions of that object have new ids.

### Deleting Objects With Object Versioning Enabled

If we attempt to delete an object with object versioning enabled and without specifying a specific version you’d like to delete, S3 will add a new special version of that object known as a _delete marker_.

The delete marker is a new version of the object that makes the object look deleted, but in reality the object is just hidden.
If the delete marker is deleted, the object is returned to being in a normal active state.
To delete an object, we need to specify a particular version ID.

### MFA Delete

MFA Delete is a feature that can be enabled to require MFA to change bucket versioning states, or to fully delete versions of objects. Enabled in versioning configuration. Serial number + Code passed with API calls are needed. 

OBJECT VERSIONING 
- cannot be switched off only suspended 
- space is consumed by all versions 
- only way to 0 costs is to delete the bucket, billed for ALL versions 


