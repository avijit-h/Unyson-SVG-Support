# Unyson-SVG-Support
This modified Unyson plugin ensures that SVG images in the fw-backup zip file are retained during content or full backups.

Added pathinfo($file_path, PATHINFO_EXTENSION) !== 'svg' on line number 88 
\unyson\framework\extensions\backups\includes\module\tasks\type\class-fw-ext-backups-task-type-image-sizes-remove.php

if (file_exists($file_path) && pathinfo($file_path, PATHINFO_EXTENSION) !== 'svg' ) {
  @unlink( $file_path );
}
