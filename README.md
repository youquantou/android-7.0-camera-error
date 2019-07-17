# android-7.0-camera-error
高版本android 调用系统相机bug


1.在res下创建xml/file_paths
<?xml version="1.0" encoding="utf-8"?>
<paths>

    <root-path name="camera_p"
        path=""/>

</paths>

2.在application标签下添加
       <provider
            android:name="android.support.v4.content.FileProvider"
            android:authorities="com.jni_text.jyl.ailock.fileprovider"
            android:exported="false"
            android:grantUriPermissions="true">
            <meta-data
                android:name="android.support.FILE_PROVIDER_PATHS"
                android:resource="@xml/file_paths" />
        </provider>
