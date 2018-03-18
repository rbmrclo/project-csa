# RDS Backups

- AWS provides automated point-in-time backups against the RDS database instance.
- Automated backups are deleted once the database instance is deleted and cannot
  be recovered (but you can take your own snapshots of backups before deleting).
- Backups on database engines only work correctly when the database engine is
  "transactional", but do currently work for all supported database types.
- MySQL requires InnoDB for reliable backups.
