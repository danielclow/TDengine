---
title: TDengine Command Line (CLI)
sidebar_label: TDengine CLI
description: Instructions and tips for using the TDengine CLI to connect TDengine Cloud
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

The TDengine command-line interface (hereafter referred to as `TDengine CLI`) is the most simplest way for users to manipulate and interact with TDengine instances.

## Installation

To run TDengine CLI to access TDengine cloud, please install [TDengine client installation package](https://gcp.cloud.tdengine.com/download/TDengine-client-2.7.0.0-Linux-x64.tar.gz) first.

## Config

<Tabs defaultValue="linux" groupId="sys">
<TabItem value="linux" label="Config on Linux">

Run this command in your Linux terminal to save your URL and token as variable:

```bash
export TDENGINE_CLOUD_DSN="<DSN>"
```

</TabItem>
<TabItem value="windows" label="Config on Windows (coming soon)">

Run this command in your Windows terminal to save your URL and token as variable:

```bash
set TDENGINE_CLOUD_DSN="<DSN>"
```

</TabItem>
<TabItem value="mac" label="Config on Mac (coming soon)" groupId="sys">

Run this command in your Mac terminal to save your URL and token as variable:

```bash
export TDENGINE_CLOUD_DSN="<DSN>"
```

</TabItem>
</Tabs>

## Connect 

<Tabs defaultValue="linux" groupId="sys">
<TabItem value="linux" label="Connect on Linux">

To access the TDengine Cloud, you can execute `taos` if you already set the environment variable.

```
taos
```

If you did not set environment variable for a TDengine Cloud instance, or you want to access other TDengine Cloud instances rather than the instance you already set the environment variable, you can use `taos -E <DSN>` as below.

```
taos -E $TDENGINE_CLOUD_DSN
```

</TabItem>
<TabItem value="windows" label="Connect on Windows (coming soon)">

To access the TDengine Cloud, you can execute `taos` if you already set the environment variable.

```
taos
```

If you did not set environment variable for a TDengine Cloud instance, or you want to access other TDengine Cloud instances rather than the instance you already set the environment variable, you can use `taos -E <DSN>` as below.

```
taos.exe -E $TDENGINE_CLOUD_DSN
```

</TabItem>
<TabItem value="mac" label="Connect on Mac (coming soon)">

To access the TDengine Cloud, you can execute `taos` if you already set the environment variable.

```
taos
```

If you did not set environment variable for a TDengine Cloud instance, or you want to access other TDengine Cloud instances rather than the instance you already set the environment variable, you can use `taos -E <DSN>` as below.

```
taos -E $TDENGINE_CLOUD_DSN
```

</TabItem>
</Tabs>

## Using TDengine CLI

TDengine CLI will display a welcome message and version information if it successfully connected to the TDengine service. If it fails, TDengine CLI will print an error message. See [FAQ](/train-faq/faq) to solve the problem of terminal connection failure to the server. The TDengine CLI prompts as follows:

```
Welcome to the TDengine shell from Linux, Client Version:2.6.0.4
Copyright (c) 2022 by TAOS Data, Inc. All rights reserved.

Successfully connect to cloud.tdengine.com:8085 in restful mode

taos>
```

After entering the TDengine CLI, you can execute various SQL commands, including inserts, queries, or administrative commands. Please see the [official document](https://docs.tdengine.com/reference/taos-shell#execute-sql-script-file) for more details.
