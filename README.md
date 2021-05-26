# aws-team3_project-rds

module "rds_cluster" {
  source  = "Matii84/rds_cluster/aws"
  version = "1.0.0" 
  
  cluster_identifier      = "aurora-cluster-demo"
  engine                  = "aurora-mysql"
  engine_version          = "5.7.mysql_aurora.2.07.2"
  availability_zones      = ["us-east-2a", "us-east-2b", "us-east-2c"]
  database_name           = "db"
  master_username         = "foo"
  master_password         = "MYPROJECT"
  preferred_backup_window = "07:00-09:00"
  skip_final_snapshot  = true
  region = "us-east-2"      
}