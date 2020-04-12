# api

https://docs.openstack.org/api-ref/identity/v3/index.html?expanded=password-authentication-with-unscoped-authorization-detail,password-authentication-with-scoped-authorization-detail,password-authentication-with-explicit-unscoped-authorization-detail,token-authentication-with-unscoped-authorization-detail,token-authentication-with-scoped-authorization-detail,token-authentication-with-explicit-unscoped-authorization-detail,multi-step-authentication-2-factor-password-and-totp-example-detail,validate-and-show-information-for-token-detail,check-token-detail,revoke-token-detail,get-service-catalog-detail,get-available-project-scopes-detail,get-available-domain-scopes-detail,get-available-system-scopes-detail,authenticating-with-an-application-credential-detail,create-application-credential-detail,list-application-credentials-detail,show-application-credential-details-detail,delete-application-credential-detail,list-access-rules-detail,show-access-rule-details-detail,delete-access-rule-detail,create-credential-detail,list-credentials-detail,show-credential-details-detail,update-credential-detail,delete-credential-detail,list-domains-detail,create-domain-detail,show-domain-details-detail,update-domain-detail,delete-domain-detail,show-default-configuration-settings-detail,show-default-configuration-for-a-group-detail,show-default-option-for-a-group-detail,show-domain-group-option-configuration-detail,update-domain-group-option-configuration-detail,delete-domain-group-option-configuration-detail,show-domain-group-configuration-detail,update-domain-group-configuration-detail,delete-domain-group-configuration-detail,create-domain-configuration-detail,show-domain-configuration-detail,update-domain-configuration-detail,delete-domain-configuration-detail,list-groups-detail,create-group-detail,show-group-details-detail,update-group-detail,delete-group-detail,list-users-in-group-detail,add-user-to-group-detail,check-whether-user-belongs-to-group-detail,remove-user-from-group-detail,assign-role-to-user-on-projects-owned-by-domain-detail,assign-role-to-group-on-projects-owned-by-a-domain-detail,list-user-s-inherited-project-roles-on-a-domain-detail,list-group-s-inherited-project-roles-on-domain-detail,check-if-user-has-an-inherited-project-role-on-domain-detail,check-if-group-has-an-inherited-project-role-on-domain-detail,revoke-an-inherited-project-role-from-user-on-domain-detail,revoke-an-inherited-project-role-from-group-on-domain-detail,assign-role-to-user-on-projects-in-a-subtree-detail,assign-role-to-group-on-projects-in-a-subtree-detail,check-if-user-has-an-inherited-project-role-on-project-detail,check-if-group-has-an-inherited-project-role-on-project-detail,revoke-an-inherited-project-role-from-user-on-project-detail,revoke-an-inherited-project-role-from-group-on-project-detail,list-role-assignments-detail,list-revoked-tokens-detail,create-policy-detail,list-policies-detail,show-policy-details-detail,update-policy-detail,delete-policy-detail,list-projects-detail,create-project-detail,show-project-details-detail,update-project-detail,delete-project-detail,list-tags-for-a-project-detail,modify-tag-list-for-a-project-detail,remove-all-tags-from-a-project-detail,check-if-project-contains-tag-detail,add-single-tag-to-a-project-detail,delete-single-tag-from-project-detail,show-region-details-detail,update-region-detail,delete-region-detail,list-regions-detail,create-region-detail,list-roles-detail,create-role-detail,show-role-details-detail,update-role-detail,delete-role-detail,list-role-assignments-for-group-on-domain-detail,assign-role-to-group-on-domain-detail,check-whether-group-has-role-assignment-on-domain-detail,unassign-role-from-group-on-domain-detail,list-role-assignments-for-user-on-domain-detail,assign-role-to-user-on-domain-detail,check-whether-user-has-role-assignment-on-domain-detail,unassigns-role-from-user-on-domain-detail,list-role-assignments-for-group-on-project-detail,assign-role-to-group-on-project-detail,check-whether-group-has-role-assignment-on-project-detail,unassign-role-from-group-on-project-detail,list-role-assignments-for-user-on-project-detail,assign-role-to-user-on-project-detail,check-whether-user-has-role-assignment-on-project-detail,unassign-role-from-user-on-project-detail,list-implied-inference-roles-for-role-detail,create-role-inference-rule-detail,get-role-inference-rule-detail,confirm-role-inference-rule-detail,delete-role-inference-rule-detail,id627-detail,list-all-role-inference-rules-detail,list-system-role-assignments-for-a-user-detail,assign-a-system-role-to-a-user-detail,check-user-for-a-system-role-assignment-detail,get-system-role-assignment-for-a-user-detail,delete-a-system-role-assignment-from-a-user-detail,list-system-role-assignments-for-a-group-detail,assign-a-system-role-to-a-group-detail,check-group-for-a-system-role-assignment-detail,get-system-role-assignment-for-a-group-detail,delete-a-system-role-assignment-from-a-group-detail,list-services-detail,create-service-detail,show-service-details-detail,update-service-detail,delete-service-detail,list-endpoints-detail,create-endpoint-detail,show-endpoint-details-detail,update-endpoint-detail,delete-endpoint-detail,list-registered-limits-detail,create-registered-limits-detail,update-registered-limits-detail,show-registered-limit-details-detail,delete-registered-limit-detail,get-enforcement-model-detail,list-limits-detail,create-limits-detail,update-limits-detail,show-limit-details-detail,id799-detail,list-users-detail,create-user-detail,show-user-details-detail,update-user-detail,delete-user-detail,list-groups-to-which-a-user-belongs-detail,list-projects-for-user-detail,change-password-for-user-detail#relationships

### /v3/auth/tokens POST

- req

```
{
    "auth": {
        "identity": {
            "methods": [
                "password"
            ],
            "password": {
                "user": {
                    "name": "admin",
                    "domain": {
                        "name": "Default"
                    },
                    "password": "devstacker"
                }
            }
        }
    }
}
```

- res

```
{
"token":{
"issued_at": "2020-04-12T05:11:00.000000Z",
"audit_ids":[
"_Qeg5hAPQQu_7aVgSC3NVQ"
],
"methods":[
"password"
],
"expires_at": "2020-04-12T06:11:00.000000Z",
"user":{"password_expires_at": null, "domain":{"id": "default", "name": "Default"…}
}
}
```

- dblog

```
2020-04-12T05:10:58.303112Z	    5 Connect	keystone@localhost on keystone using TCP/IP
2020-04-12T05:10:58.313213Z	    5 Query	SET AUTOCOMMIT = 0
2020-04-12T05:10:58.325203Z	    5 Query	SHOW VARIABLES LIKE 'sql_mode'
2020-04-12T05:10:58.352469Z	    5 Query	SELECT VERSION()
2020-04-12T05:10:58.355378Z	    5 Query	SELECT DATABASE()
2020-04-12T05:10:58.356366Z	    5 Query	SELECT @@transaction_isolation
2020-04-12T05:10:58.361365Z	    5 Query	show collation where `Charset` = 'utf8' and `Collation` = 'utf8_bin'
2020-04-12T05:10:58.449554Z	    5 Query	SELECT CAST('test plain returns' AS CHAR(60)) AS anon_1
2020-04-12T05:10:58.450431Z	    5 Query	SELECT CAST('test unicode returns' AS CHAR(60)) AS anon_1
2020-04-12T05:10:58.454501Z	    5 Query	SELECT CAST('test collated returns' AS CHAR CHARACTER SET utf8) COLLATE utf8_bin AS anon_1
2020-04-12T05:10:58.455789Z	    5 Query	ROLLBACK
2020-04-12T05:10:58.456755Z	    5 Query	SET SESSION sql_mode = 'TRADITIONAL'
2020-04-12T05:10:58.457706Z	    5 Query	SHOW VARIABLES LIKE 'sql_mode'
2020-04-12T05:10:58.461077Z	    5 Query	SET SESSION sql_mode = 'TRADITIONAL'
2020-04-12T05:10:58.474498Z	    5 Query	SELECT 1
2020-04-12T05:10:58.475395Z	    5 Query	ROLLBACK
2020-04-12T05:10:59.241372Z	    5 Query	SELECT 1
2020-04-12T05:10:59.247503Z	    5 Query	SELECT project.id AS project_id, project.name AS project_name, project.domain_id AS project_domain_id, project.description AS project_description, project.enabled AS project_enabled, project.extra AS project_extra, project.parent_id AS project_parent_id, project.is_domain AS project_is_domain
FROM project
WHERE project.name = 'Default' AND project.domain_id = '<<keystone.domain.root>>'
2020-04-12T05:10:59.274582Z	    5 Query	SELECT project_tag.project_id AS project_tag_project_id, project_tag.name AS project_tag_name, anon_1.project_id AS anon_1_project_id
FROM (SELECT project.id AS project_id
FROM project
WHERE project.name = 'Default' AND project.domain_id = '<<keystone.domain.root>>') AS anon_1 INNER JOIN project_tag ON project_tag.project_id = anon_1.project_id ORDER BY anon_1.project_id
2020-04-12T05:10:59.295017Z	    5 Query	ROLLBACK
2020-04-12T05:10:59.336683Z	    5 Query	SELECT 1
2020-04-12T05:10:59.338915Z	    5 Query	SELECT user.enabled AS user_enabled, user.id AS user_id, user.domain_id AS user_domain_id, user.extra AS user_extra, user.default_project_id AS user_default_project_id, user.created_at AS user_created_at, user.last_active_at AS user_last_active_at
FROM user INNER JOIN local_user ON user.id = local_user.user_id AND user.domain_id = local_user.domain_id
WHERE local_user.name = 'admin' AND local_user.domain_id = 'default'
2020-04-12T05:10:59.343902Z	    5 Query	SELECT user_option.user_id AS user_option_user_id, user_option.option_id AS user_option_option_id, user_option.option_value AS user_option_option_value, anon_1.user_id AS anon_1_user_id
FROM (SELECT user.id AS user_id
FROM user INNER JOIN local_user ON user.id = local_user.user_id AND user.domain_id = local_user.domain_id
WHERE local_user.name = 'admin' AND local_user.domain_id = 'default') AS anon_1 INNER JOIN user_option ON anon_1.user_id = user_option.user_id ORDER BY anon_1.user_id
2020-04-12T05:10:59.357365Z	    5 Query	SELECT local_user.id AS local_user_id, local_user.user_id AS local_user_user_id, local_user.domain_id AS local_user_domain_id, local_user.name AS local_user_name, local_user.failed_auth_count AS local_user_failed_auth_count, local_user.failed_auth_at AS local_user_failed_auth_at, anon_1.user_domain_id AS anon_1_user_domain_id, anon_1.user_id AS anon_1_user_id
FROM (SELECT user.domain_id AS user_domain_id, user.id AS user_id
FROM user INNER JOIN local_user ON user.id = local_user.user_id AND user.domain_id = local_user.domain_id
WHERE local_user.name = 'admin' AND local_user.domain_id = 'default') AS anon_1 INNER JOIN local_user ON anon_1.user_id = local_user.user_id AND anon_1.user_domain_id = local_user.domain_id ORDER BY anon_1.user_domain_id, anon_1.user_id
2020-04-12T05:10:59.361061Z	    5 Query	SELECT password.created_at AS password_created_at, password.expires_at AS password_expires_at, password.id AS password_id, password.local_user_id AS password_local_user_id, password.password AS password_password, password.password_hash AS password_password_hash, password.created_at_int AS password_created_at_int, password.expires_at_int AS password_expires_at_int, password.self_service AS password_self_service, local_user_1.id AS local_user_1_id
FROM (SELECT user.domain_id AS user_domain_id, user.id AS user_id
FROM user INNER JOIN local_user ON user.id = local_user.user_id AND user.domain_id = local_user.domain_id
WHERE local_user.name = 'admin' AND local_user.domain_id = 'default') AS anon_1 INNER JOIN local_user AS local_user_1 ON anon_1.user_id = local_user_1.user_id AND anon_1.user_domain_id = local_user_1.domain_id INNER JOIN password ON local_user_1.id = password.local_user_id ORDER BY local_user_1.id, password.created_at_int
2020-04-12T05:10:59.375832Z	    5 Query	SELECT federated_user.id AS federated_user_id, federated_user.user_id AS federated_user_user_id, federated_user.idp_id AS federated_user_idp_id, federated_user.protocol_id AS federated_user_protocol_id, federated_user.unique_id AS federated_user_unique_id, federated_user.display_name AS federated_user_display_name, anon_1.user_id AS anon_1_user_id
FROM (SELECT user.id AS user_id
FROM user INNER JOIN local_user ON user.id = local_user.user_id AND user.domain_id = local_user.domain_id
WHERE local_user.name = 'admin' AND local_user.domain_id = 'default') AS anon_1 INNER JOIN federated_user ON anon_1.user_id = federated_user.user_id ORDER BY anon_1.user_id
2020-04-12T05:10:59.379979Z	    5 Query	SELECT nonlocal_user.domain_id AS nonlocal_user_domain_id, nonlocal_user.name AS nonlocal_user_name, nonlocal_user.user_id AS nonlocal_user_user_id, anon_1.user_domain_id AS anon_1_user_domain_id, anon_1.user_id AS anon_1_user_id
FROM (SELECT user.domain_id AS user_domain_id, user.id AS user_id
FROM user INNER JOIN local_user ON user.id = local_user.user_id AND user.domain_id = local_user.domain_id
WHERE local_user.name = 'admin' AND local_user.domain_id = 'default') AS anon_1 INNER JOIN nonlocal_user ON anon_1.user_domain_id = nonlocal_user.domain_id AND anon_1.user_id = nonlocal_user.user_id ORDER BY anon_1.user_domain_id, anon_1.user_id
2020-04-12T05:10:59.388867Z	    5 Query	ROLLBACK
2020-04-12T05:10:59.399538Z	    5 Query	SELECT 1
2020-04-12T05:10:59.400565Z	    5 Query	SELECT project.id AS project_id, project.name AS project_name, project.domain_id AS project_domain_id, project.description AS project_description, project.enabled AS project_enabled, project.extra AS project_extra, project.parent_id AS project_parent_id, project.is_domain AS project_is_domain
FROM project
WHERE project.id = 'default'
2020-04-12T05:10:59.402907Z	    5 Query	SELECT project_tag.project_id AS project_tag_project_id, project_tag.name AS project_tag_name, anon_1.project_id AS anon_1_project_id
FROM (SELECT project.id AS project_id
FROM project
WHERE project.id = 'default') AS anon_1 INNER JOIN project_tag ON project_tag.project_id = anon_1.project_id ORDER BY anon_1.project_id
2020-04-12T05:10:59.403845Z	    5 Query	ROLLBACK
2020-04-12T05:10:59.426921Z	    5 Query	SELECT 1
2020-04-12T05:10:59.427749Z	    5 Query	SELECT user.enabled AS user_enabled, user.id AS user_id, user.domain_id AS user_domain_id, user.extra AS user_extra, user.default_project_id AS user_default_project_id, user.created_at AS user_created_at, user.last_active_at AS user_last_active_at
FROM user
WHERE user.id = '94bcf191c28a4db89301999207b6531f'
2020-04-12T05:10:59.429581Z	    5 Query	SELECT user_option.user_id AS user_option_user_id, user_option.option_id AS user_option_option_id, user_option.option_value AS user_option_option_value, anon_1.user_id AS anon_1_user_id
FROM (SELECT user.id AS user_id
FROM user
WHERE user.id = '94bcf191c28a4db89301999207b6531f') AS anon_1 INNER JOIN user_option ON anon_1.user_id = user_option.user_id ORDER BY anon_1.user_id
2020-04-12T05:10:59.434382Z	    5 Query	SELECT local_user.id AS local_user_id, local_user.user_id AS local_user_user_id, local_user.domain_id AS local_user_domain_id, local_user.name AS local_user_name, local_user.failed_auth_count AS local_user_failed_auth_count, local_user.failed_auth_at AS local_user_failed_auth_at, anon_1.user_domain_id AS anon_1_user_domain_id, anon_1.user_id AS anon_1_user_id
FROM (SELECT user.domain_id AS user_domain_id, user.id AS user_id
FROM user
WHERE user.id = '94bcf191c28a4db89301999207b6531f') AS anon_1 INNER JOIN local_user ON anon_1.user_id = local_user.user_id AND anon_1.user_domain_id = local_user.domain_id ORDER BY anon_1.user_domain_id, anon_1.user_id
2020-04-12T05:10:59.436605Z	    5 Query	SELECT password.created_at AS password_created_at, password.expires_at AS password_expires_at, password.id AS password_id, password.local_user_id AS password_local_user_id, password.password AS password_password, password.password_hash AS password_password_hash, password.created_at_int AS password_created_at_int, password.expires_at_int AS password_expires_at_int, password.self_service AS password_self_service, local_user_1.id AS local_user_1_id
FROM (SELECT user.domain_id AS user_domain_id, user.id AS user_id
FROM user
WHERE user.id = '94bcf191c28a4db89301999207b6531f') AS anon_1 INNER JOIN local_user AS local_user_1 ON anon_1.user_id = local_user_1.user_id AND anon_1.user_domain_id = local_user_1.domain_id INNER JOIN password ON local_user_1.id = password.local_user_id ORDER BY local_user_1.id, password.created_at_int
2020-04-12T05:10:59.438840Z	    5 Query	SELECT federated_user.id AS federated_user_id, federated_user.user_id AS federated_user_user_id, federated_user.idp_id AS federated_user_idp_id, federated_user.protocol_id AS federated_user_protocol_id, federated_user.unique_id AS federated_user_unique_id, federated_user.display_name AS federated_user_display_name, anon_1.user_id AS anon_1_user_id
FROM (SELECT user.id AS user_id
FROM user
WHERE user.id = '94bcf191c28a4db89301999207b6531f') AS anon_1 INNER JOIN federated_user ON anon_1.user_id = federated_user.user_id ORDER BY anon_1.user_id
2020-04-12T05:10:59.440683Z	    5 Query	SELECT nonlocal_user.domain_id AS nonlocal_user_domain_id, nonlocal_user.name AS nonlocal_user_name, nonlocal_user.user_id AS nonlocal_user_user_id, anon_1.user_domain_id AS anon_1_user_domain_id, anon_1.user_id AS anon_1_user_id
FROM (SELECT user.domain_id AS user_domain_id, user.id AS user_id
FROM user
WHERE user.id = '94bcf191c28a4db89301999207b6531f') AS anon_1 INNER JOIN nonlocal_user ON anon_1.user_domain_id = nonlocal_user.domain_id AND anon_1.user_id = nonlocal_user.user_id ORDER BY anon_1.user_domain_id, anon_1.user_id
2020-04-12T05:10:59.441694Z	    5 Query	ROLLBACK
2020-04-12T05:10:59.450648Z	    5 Query	SELECT 1
2020-04-12T05:10:59.451497Z	    5 Query	SELECT user.enabled AS user_enabled, user.id AS user_id, user.domain_id AS user_domain_id, user.extra AS user_extra, user.default_project_id AS user_default_project_id, user.created_at AS user_created_at, user.last_active_at AS user_last_active_at
FROM user
WHERE user.id = '94bcf191c28a4db89301999207b6531f'
2020-04-12T05:10:59.453280Z	    5 Query	SELECT user_option.user_id AS user_option_user_id, user_option.option_id AS user_option_option_id, user_option.option_value AS user_option_option_value, anon_1.user_id AS anon_1_user_id
FROM (SELECT user.id AS user_id
FROM user
WHERE user.id = '94bcf191c28a4db89301999207b6531f') AS anon_1 INNER JOIN user_option ON anon_1.user_id = user_option.user_id ORDER BY anon_1.user_id
2020-04-12T05:10:59.458415Z	    5 Query	SELECT local_user.id AS local_user_id, local_user.user_id AS local_user_user_id, local_user.domain_id AS local_user_domain_id, local_user.name AS local_user_name, local_user.failed_auth_count AS local_user_failed_auth_count, local_user.failed_auth_at AS local_user_failed_auth_at, anon_1.user_domain_id AS anon_1_user_domain_id, anon_1.user_id AS anon_1_user_id
FROM (SELECT user.domain_id AS user_domain_id, user.id AS user_id
FROM user
WHERE user.id = '94bcf191c28a4db89301999207b6531f') AS anon_1 INNER JOIN local_user ON anon_1.user_id = local_user.user_id AND anon_1.user_domain_id = local_user.domain_id ORDER BY anon_1.user_domain_id, anon_1.user_id
2020-04-12T05:10:59.460790Z	    5 Query	SELECT password.created_at AS password_created_at, password.expires_at AS password_expires_at, password.id AS password_id, password.local_user_id AS password_local_user_id, password.password AS password_password, password.password_hash AS password_password_hash, password.created_at_int AS password_created_at_int, password.expires_at_int AS password_expires_at_int, password.self_service AS password_self_service, local_user_1.id AS local_user_1_id
FROM (SELECT user.domain_id AS user_domain_id, user.id AS user_id
FROM user
WHERE user.id = '94bcf191c28a4db89301999207b6531f') AS anon_1 INNER JOIN local_user AS local_user_1 ON anon_1.user_id = local_user_1.user_id AND anon_1.user_domain_id = local_user_1.domain_id INNER JOIN password ON local_user_1.id = password.local_user_id ORDER BY local_user_1.id, password.created_at_int
2020-04-12T05:10:59.462843Z	    5 Query	SELECT federated_user.id AS federated_user_id, federated_user.user_id AS federated_user_user_id, federated_user.idp_id AS federated_user_idp_id, federated_user.protocol_id AS federated_user_protocol_id, federated_user.unique_id AS federated_user_unique_id, federated_user.display_name AS federated_user_display_name, anon_1.user_id AS anon_1_user_id
FROM (SELECT user.id AS user_id
FROM user
WHERE user.id = '94bcf191c28a4db89301999207b6531f') AS anon_1 INNER JOIN federated_user ON anon_1.user_id = federated_user.user_id ORDER BY anon_1.user_id
2020-04-12T05:10:59.464561Z	    5 Query	SELECT nonlocal_user.domain_id AS nonlocal_user_domain_id, nonlocal_user.name AS nonlocal_user_name, nonlocal_user.user_id AS nonlocal_user_user_id, anon_1.user_domain_id AS anon_1_user_domain_id, anon_1.user_id AS anon_1_user_id
FROM (SELECT user.domain_id AS user_domain_id, user.id AS user_id
FROM user
WHERE user.id = '94bcf191c28a4db89301999207b6531f') AS anon_1 INNER JOIN nonlocal_user ON anon_1.user_domain_id = nonlocal_user.domain_id AND anon_1.user_id = nonlocal_user.user_id ORDER BY anon_1.user_domain_id, anon_1.user_id
2020-04-12T05:10:59.465941Z	    5 Query	ROLLBACK
2020-04-12T05:10:59.970714Z	    5 Query	SELECT 1
2020-04-12T05:10:59.972118Z	    5 Query	SELECT user.enabled AS user_enabled, user.id AS user_id, user.domain_id AS user_domain_id, user.extra AS user_extra, user.default_project_id AS user_default_project_id, user.created_at AS user_created_at, user.last_active_at AS user_last_active_at
FROM user
WHERE user.id = '94bcf191c28a4db89301999207b6531f'
2020-04-12T05:10:59.973852Z	    5 Query	SELECT user_option.user_id AS user_option_user_id, user_option.option_id AS user_option_option_id, user_option.option_value AS user_option_option_value, anon_1.user_id AS anon_1_user_id
FROM (SELECT user.id AS user_id
FROM user
WHERE user.id = '94bcf191c28a4db89301999207b6531f') AS anon_1 INNER JOIN user_option ON anon_1.user_id = user_option.user_id ORDER BY anon_1.user_id
2020-04-12T05:10:59.978135Z	    5 Query	SELECT local_user.id AS local_user_id, local_user.user_id AS local_user_user_id, local_user.domain_id AS local_user_domain_id, local_user.name AS local_user_name, local_user.failed_auth_count AS local_user_failed_auth_count, local_user.failed_auth_at AS local_user_failed_auth_at, anon_1.user_domain_id AS anon_1_user_domain_id, anon_1.user_id AS anon_1_user_id
FROM (SELECT user.domain_id AS user_domain_id, user.id AS user_id
FROM user
WHERE user.id = '94bcf191c28a4db89301999207b6531f') AS anon_1 INNER JOIN local_user ON anon_1.user_id = local_user.user_id AND anon_1.user_domain_id = local_user.domain_id ORDER BY anon_1.user_domain_id, anon_1.user_id
2020-04-12T05:10:59.979998Z	    5 Query	SELECT password.created_at AS password_created_at, password.expires_at AS password_expires_at, password.id AS password_id, password.local_user_id AS password_local_user_id, password.password AS password_password, password.password_hash AS password_password_hash, password.created_at_int AS password_created_at_int, password.expires_at_int AS password_expires_at_int, password.self_service AS password_self_service, local_user_1.id AS local_user_1_id
FROM (SELECT user.domain_id AS user_domain_id, user.id AS user_id
FROM user
WHERE user.id = '94bcf191c28a4db89301999207b6531f') AS anon_1 INNER JOIN local_user AS local_user_1 ON anon_1.user_id = local_user_1.user_id AND anon_1.user_domain_id = local_user_1.domain_id INNER JOIN password ON local_user_1.id = password.local_user_id ORDER BY local_user_1.id, password.created_at_int
2020-04-12T05:10:59.981918Z	    5 Query	SELECT federated_user.id AS federated_user_id, federated_user.user_id AS federated_user_user_id, federated_user.idp_id AS federated_user_idp_id, federated_user.protocol_id AS federated_user_protocol_id, federated_user.unique_id AS federated_user_unique_id, federated_user.display_name AS federated_user_display_name, anon_1.user_id AS anon_1_user_id
FROM (SELECT user.id AS user_id
FROM user
WHERE user.id = '94bcf191c28a4db89301999207b6531f') AS anon_1 INNER JOIN federated_user ON anon_1.user_id = federated_user.user_id ORDER BY anon_1.user_id
2020-04-12T05:10:59.983516Z	    5 Query	SELECT nonlocal_user.domain_id AS nonlocal_user_domain_id, nonlocal_user.name AS nonlocal_user_name, nonlocal_user.user_id AS nonlocal_user_user_id, anon_1.user_domain_id AS anon_1_user_domain_id, anon_1.user_id AS anon_1_user_id
FROM (SELECT user.domain_id AS user_domain_id, user.id AS user_id
FROM user
WHERE user.id = '94bcf191c28a4db89301999207b6531f') AS anon_1 INNER JOIN nonlocal_user ON anon_1.user_domain_id = nonlocal_user.domain_id AND anon_1.user_id = nonlocal_user.user_id ORDER BY anon_1.user_domain_id, anon_1.user_id
2020-04-12T05:10:59.984394Z	    5 Query	ROLLBACK
2020-04-12T05:11:00.127019Z	    5 Query	SELECT 1
2020-04-12T05:11:00.128994Z	    5 Query	SELECT service_provider.id AS service_provider_id, service_provider.enabled AS service_provider_enabled, service_provider.description AS service_provider_description, service_provider.auth_url AS service_provider_auth_url, service_provider.sp_url AS service_provider_sp_url, service_provider.relay_state_prefix AS service_provider_relay_state_prefix
FROM service_provider
WHERE service_provider.enabled = true
2020-04-12T05:11:00.130702Z	    5 Query	ROLLBACK
```

