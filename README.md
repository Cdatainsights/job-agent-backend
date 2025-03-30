cd job-agent-backend

then do 

python -m venv venv
source venv/bin/activate                    ### fro dhruv  source venv/bin/activate.fish ##
pip install -r requirements.txt

npm run dev                                 ###for auto start 

npm run start                               ### for background start (server only]


for running on terminal local host 3k : uv run python -m uvicorn api.index:app --reload --host 0.0.0.0 --port 8000
for running on bg : nohup uv run python -m uvicorn api.index:app --host 0.0.0.0 --port 8000 & disown

how to stop bg version
ps aux | grep uvicorn
kill <PID>
 this should start it on port 8000